# An RDF based ontology for the modeling of networks of slaveholding and enslavement in the Genoese Mediterranean

This appendix describes the modeling of persons, places, and contracts that form the backbone of the online database *Networks of slaveholding and enslavement in the Genoese Mediterranean, 1348–1528* that was developed as a companion to this study. It is intended as a reference document to illustrate how the existing CIDOC-CRM Conceptual Framework, which was developed for cultural institutions, can be extended to model historical events, documents, and persons. The online database can be accessed at:

http://www.genoesemerchantnetworks.com/omeka-s/s/main/page/welcome

The ontology that extends CIDOC-CRM and upon which this database is constructed is named GEMENET. The ontology definition and namespace is available at:

https://ontome.net/namespace/192

This ontology, as mentioned above, is an extension of the CIDOC-CRM 7.1.1 Conceptual Reference Model ontology.[[1\]](#_ftn1) The default CIDOC-CRM 7.1.1 classes and properties are available at:

https://cidoc-crm.org/html/cidoc_crm_v7.1.1.html

The online database intended as a companion for this thesis maps the social networks of thousands of slaveholders and enslaved persons attested in Genoese notarial contracts. As of July 2022 this database has encoded the following entities.

- 8578 historical persons
- 1824 notarial contracts
- 6 socioeconomic institutions

As of July 2022 this database has encoded the following relationships.

- 3204 parental relationships
- 1949 marriage relationships
- 7853 contractual relationships
- 54 institutional relationships

## I. Classes

This section defines the classes in the GEMENET ontology. These classes are extensions of classes delineated in the CIDOC-CRM 7.1.1 ontology.

### Class hierarchy

The class hierarchy is shown below.

```
E7 Activity
	Transactio
		Acordatio
			Compromissum
		Arbitratio
		Asecuratio
		Cassatio
		Cessio
		Datio
		Debitum
		Dos
		Franchixia
		Inventarium
		Locatio
		Procura
		Promissio
		Quitatio
		Sententia
		Societas
		Testamentum
		Testimonium
		Venditio
E21 Person
	Person
E53 Place
	Place
E74 Group
	Gender
	Nationality
	Occupational Group
	Organization
	Social Category
E71 Human-Made Thing
	Asset
	Commodity
	Property
	Real Estate
	Equity
	Fixed Income
	Money
	Real Estate
	Archival Item
```

### Description of classes

#### Acordatio (a mutual agreement)

Subclass of:

```
Transactio
```

Superclass of:

```
Compromissum
```

Scope note:

An `Acordatio` was a mutual agreement between two or more parties. In abstract terms, it is a unilateral transaction where two or more parties agree regarding ownership and rights over object of agreement.

Properties:

```
has party to agreement
has object of agreement
```

#### Arbitratio (an arbitration)

Subclass of:
	`Transactio`

Scope note:

An `Arbitratio` is a ruling or sentence of an arbitrator. In this transaction an arbitrator issues a judgment to the parties of an arbitration. This generally involves two or more parties who have a business conflict of some sort or another. In abstract terms, the arbitrator is transferring a judgment of arbitration to the parties of arbitration.

Properties:

```
has arbitrator
has party to arbitration
has object of arbitration
```

#### Asecuratio (an act of insurance)

Subclass of:

```
Transactio
```

Scope note:

An `Asecuratio` is the insurance of an object or person by an underwriter. In this transaction an underwriter provides insurance on something for someone who is purchasing the insurance. In abstract terms, the underwriter is transferring a guarantee of insurance to the buyer of the insurance. This act of insurance is also titled *securitas*.

Properties:

```
has underwriter
has buyer
has object of insurance
```

#### Cassatio (an annulment)

Subclass of:

```
Transactio
```

Scope note:

A `Cassatio` is the annulment of some previously contracted agreement between two or more parties. In abstract terms, the original primary transactor is transferring an agreement of annulment to the secondary primary transactor.

Properties:

```
has primary transactor
has secondary transactor
has original contractual object
has reference to original transaction
```

#### Cessio (a cession of rights)

Subclass of:
	`Transactio`

Scope note:

A `Cessio` is the cession of rights by one party to another party over some object. In abstract terms, the ceder is transferring a set of legal rights over an object to a receiver.

Properties:

```
has ceder
has receiver
has object of cession
```

#### Compromissum (a mutual agreement to abide by an arbitration)

Subclass of:

```
Acordatio
```

Scope note:

A `Compromissum` is a mutual agreement between two or more parties, usually to abide by a subsequent judgement or arbitration. In abstract terms, the parties to the agreement are transferring the duty of arbitration regarding rights over some object to an appointed arbitrator.

Properties:

```
has party to agreement
has appointed arbitrator
has object of agreement
```

#### Corretio (a correction of a previous transaction)

A `Corretio` is a correction to a previous transaction. It takes the form and structure of the transaction that it was correcting and, as such, it is not its own class. It should be modeled in the form of the corrected transaction and indicated by the has type property. For example, a *corretio vendicionis* is a correction of an earlier sale and is should be modeled as a `Venditio` with the has type property as “Corretio vendicionis.” Likewise, a *corretio sententie* is a correction of an earlier sentence and should be modeled as a Sententia with the has type property as “Corretio sententie.”

#### Datio (a donation or a gift)

Subclass of:

```
Transactio
```

Scope note:

A `Datio` is the giving of a gift by one party to another party. In abstract terms, the donator is transferring legal ownership of an object (a gift) to the receiver at no cost. The contract recording the *datio* transaction can also be named *donatio*.

Properties:

```
has donator
has receiver
has gift
```

#### Debitum (an acknowledgment of debt)

Subclass of:

```
Transactio
```

Scope note:

A `Debitum` is an acknowledgment of debt from one party to another. In abstract terms, the debtor is acknowledging an object of debt (usually a quantity of money, but it could be any economic good) to the debt holder.

Properties:

```
has debtor
has debt holder
has object of debt
```

#### Dos (a promise of a dowry)

Subclass of:

```
Transactio
```

Scope note:

A `Dos` (or *dox*) transaction is the promise of a dowry to the husband of a woman who is about to be married. In abstract terms, the promising party transfers the object of the dowry to the person receiving the dowry. The future wife maintained a limited set of rights over the dowry, so she is named as a rights holder.

Properties:

```
has promisor
has receiver
has rights holder
has object of dowry
```

#### Franchixia (a promise of manumission)

Subclass of:

```
Transactio
```

Scope note:

A `Franchixia` transaction is the promise of manumission to an enslaved person. In abstract terms, the promising party gives the gift of freedom (enshrines them with a set of legal rights and obligations) to an enslaved person.

Properties:

```
has promisor
has receiver
```

#### Inventarium (a recording of inventory)

Subclass of:

```
Transactio
```

Scope note:

An `Inventarium` is the recording of an inventory of goods which are generally, but not always, the possessions of a deceased individual. In abstract terms, an executor is naming a recorder to conduct the inventory.

Properties:

```
has executor
has recorder of inventory
has object of inventory
has location
```

#### Locatio (a lease)

Subclass of:

```
Transactio
```

Scope note:

A `Locatio` transaction is the lease of some item of property. In abstract terms, the holder is transferring temporary legal rights over the property to the leaser. The contracts recording these transactions are sometimes termed *venditio ad tempus* (sale for a time).

Properties:

```
has holder
has receiver
has object of lease
has price
has term
```

#### Nationality (an indicator of regional provenance)

Subclass of:

```
E74 Group
```

Scope note:

This is an indicator of regional provenance expressed as a relationship between a type of form of citizenship and a geographical place. 

Properties:

```
has title
has title from source
has description
has place of origin
has unique identifier
has note
```

#### Person (an historical person)

Subclass of:

```
E21_Person
```

Scope note:

This is a prosopographical record that identifies an historical individual in the late medieval Mediterranean world.

Properties:

```
has name
has description
has name from source
has patrilineage
has gender
has loconym
has nationality
has social category
has occupation
has known date range of activity
has parent
has marriage to
has unique identifier
has note
```

#### Place (a historical place)

Subclass of:

```
E53 Place
```

Scope note:

This class refers to places mentioned in notarial contracts. These places can be nations, cities, neighbourhoods, districts, and other administrative regions.

Properties:

```
has title
has title from source
has description
has location
has geospatial location
has external reference
has unique identifier
has note
```

#### Procura (a power of attorney, legal representation)

Subclass of:

```
Transactio
```

Scope note:

A **procura** is the assignment of power of attorney to an individual. In abstract terms, the delegator is transferring legal rights to the appointed procurator to function as their representative (in the name and in the place of).

Properties:

```
has delegator
has appointed procurator
has object of procuration
```

#### Promissio (a legally binding promise)

Subclass of:

```
Transactio
```

Scope note:

A **promissio** event is the promise of one party to another party regarding something. In abstract terms, the promising party is transferring a promise to the receiving party. These are often referred to as promissory notes when referring to promises to pay money.

Properties:

```
has promisor
has receiver
has object of promise
```

#### Quitatio (a quittance, a discharge from obligation)

Subclass of:

```
Transactio
```

Scope note:

A **quitatio** is the discharging of the obligation of one party to another. In abstract terms, the issuing party is transferring the canceling of obligations to the receiving party.

Properties:

```
has issuer of quittance
has receiver of quittance
has object of quittance
```

#### Sententia (a sentence, judgment)

Subclass of:

```
Transactio
```

Scope note:

A **sententia** event is the pronouncement of a sentence or judgement and recorded as a bilateral contract of the same or similar name. In abstract terms, the sentencing party transfers their legal judgement to the plaintiff of the sentence. There are two types of **sententia**. A plaintiff-defendant form where one initiating party makes a claim against another and asks for a legal sentence. The other form of **sententia**, where two or more initiating parties ask an independent body to arbitrate a dispute between them, is an **arbitratio**, and is often called a **sententia arbitralis**, and should be modeled as such.

Properties:

```
has sentencer
has plaintiff
has defendant
```

#### Societas (a business partnership)

Subclass of:

```
Transactio
```

Scope note:

A **societas** was a business partnership enacted between two or more people who pool their capital towards some venture. This was recorded as a unilateral contract and was sometimes called an **acomendatio** or **comendatio** transaction.

Properties:

```
has partner
has object of investment
```

#### Testamentum (a last will and testament)

Subclass of:

```
Transactio
```

Scope note:

A **testamentum** was the issuing of a last will and testament. It was, in its skeletal form, the appointment of an executor by the party drawing up a will. In abstract terms, the testator transfers the legal right to an executor to manage their estate according to the instructions of the testament. This includes the naming of heirs, beneficiaries, guardians, place of burial, items of inheritance, and other stipulations.

Properties:

```
has testator
has appointed executor
has appointed guardian
has beneficiary
has heir
has item of bequest
has item of inheritance
has place of burial
```

#### Testimonium (a testimony under oath)

Subclass of:

```
Transactio
```

Scope note:

A **testimonium** is the attestation made by a testifier or witness regarding some event. In abstract terms, the party making the testimony transfers an attestation regarding the object of a testimony to the party receiving the testimony. A **testimonium** transaction is also referred to as a **testificatio** transaction.

Properties:

```
has testifier
has inquisitor
has object of testimony
```

#### Transactio (a general transaction)

Subclass of:

```
E7 Activity
```

Superclass of:

```
Acordatio
Arbitratio
Asecuratio
Cassatio
Cessio
Datio
Debitum
Dos
Franchixia
Inventarium
Locatio
Procura
Promissio
Quitatio
Sententia
Societas
Testamentum
Testimonium
Venditio
```

Scope note:

This class refers to generic notarial events—transactions—from which the specific notarial events, which take place at a specific time and place, are derived. This class can also be used to describe a contractual event in which the purpose or type of contract is not yet known. As per the CIDOC-CRM framework and principles, the **transactio** and its sub classes should be considered as activities, from which the specific types of activities are derived. The document or archival source that records the activity is the domain of the is part of archival item property.

Properties:

```
has type
has title
is enacted by
has date of transaction
has description
is part of archival item
has participant
has procurator
has consenter
has additional participant
has attested place
refers to transaction
has place of enactment
has witness
has unique identifier
has note
```

#### Venditio (a sale)

Subclass of:

```
Transactio
```

Scope note:

A **venditio** is the sale of an object or objects from a seller to a buyer. In abstract terms, the owner transfers the rights of ownership over something to a buyer.

Properties:

```
has seller
has buyer
has object of sale
has price of sale
```

## II. Properties

This section defines the properties in the GEMENET ontology. These properties are extensions of properties delineated in the CIDOC-CRM 7.1.1 ontology.

### Property hierarchy

The property hierarchy for the GEMENET ontology with references to the CIDOC-CRM superproperties is shown below.

```
P1 is identified by
	has name
	has title
P2 has type
	has gender
	has type
	has marriage to
P3 has note
	has note
P4 has time span
	has date of transaction
	has known date range of activity
P11 had participant
	has additional participant
	has appointed guardian
	has beneficiary
	has consenter
	has procurator
	has witness
	is enacted by
P22 transferred title to
	has appointed arbitrator
	has appointed executor
	has appointed procurator
	has buyer
	has debt holder
	had defendant
	has party to arbitration
	has plaintiff
	has receiver
	has recorder of inventory
	has rights holder
	has secondary transactor
P23 transferred title from
	has arbitrator
	has ceder
	has debtor
	has delegator
	has donator
	has executor
	has holder
	has partner
	has party to agreement
	has primary transactor
	has promisor
	has seller
	has underwriter
P30 transferred custody of
	has gift
	has object of agreement
	has object of arbitration
	has object of cession
	has object of debt
	has object of insurance
	has object of inventory
	has object of procuration
	has object of promise
	has object of dowry
P46 forms part of
	is part of archival item
P48 has preferred identifier (is preferred identifier of)
	has unique identifier
P67 refers to (is referred to by)
	has reference to transaction
	has reference to original transaction
P89 falls within (contains)
	has geospatial location
	has location
	has loconym
	has nationality
	has place of origin
P139 has alternative form
	has name from source
	has patrilineage
	has title from source
P152 has parent
	has parent
```

### Description of properties

The following properties are used in the GEMENET ontology and are extensions of the CIDOC-CRM 7.1.1 ontology.

#### has additional participant (participated in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Transactio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies one or more persons attested within a general transaction. This property is used in cases where an attested person is not described with any of the available properties for the event type, that is, in cases where their role is not known or not determinable.

#### has arbitrator (is an arbitrator in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Arbitratio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as arbitrators named in an **arbitratio** (an arbitration) transaction. They are the subjects of this transaction, that is, they are the ones who issue the arbitration.

Examples:

A correction to an arbitration (essentially an updated version of an arbitration) conducted on 1453-06-13 issued by the arbitrators Battista Lecavello and Benedetto de Leonardis, relating to a dispute between Meliaduce Usodimare and Pietro Usodimare regarding the payment of 44 Genoese lire, in the form of interest (*paghe*) on shares (*loce*) in the Casa di San Giorgio, modifying an earlier sentence passed on the dispute.

​	Target is the **Person** named “Battista Lecavello.”

​	Target is the **Person** named “Benedetto de Leonardis.”

#### has appointed arbitrator (is appointed as arbitrator in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Arbitratio
Compromissum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the arbitrator or arbitrators in a **compromissum** (a mutual agreement to abide by an arbitration) transaction. They are the direct objects of this type of activity, having been appointed by the parties who agree to arbitration.

Examples:

A **compromissum** conducted on 1460-01-30 between Benedetto Ittaliano and the heirs of Caterina Imperiale, which are her sons Simone, Giacomo, and Gregorio Imperiale. The agreement relates to a dispute over the goods of the deceased Lanfranco Imperiale, the spouse of Caterina. Gandolfo de Fossato and Francesco Marchesio are named as arbitrators.

​	Target is the **Person** named “Gandolfo de Fossato.”

​	Target is the **Person** named “Francesco Marchesio”.

#### has appointed executor (is appointed executor in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Testamentum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are named as the executor of a **testamentum** transaction, that is, the executor of a last will and testament. The appointed executor is the indirect object of the contract who receives the instructions of the testament from the testator.

#### has appointed guardian (is appointed guardian in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Testamentum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are named as guardians of a **testamentum** transaction, that is, the guardians of a last will and testament. The heir is named in the instructions of the testament to serve as the legal guardian to the children of the testator after his or her death until they reach the age of majority.

#### has appointed procurator (is appointed as procurator in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Procura
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies a person or persons named in a **procura** (procuration or power of attorney) transaction to serve as a legal representative for another person. The appointed procurator is the indirect object of the contract who receives the right of procuration from the delegator.

#### has attested place (is attested place in)

Subproperty of:

```
P67 refers to (is referred to by)
```

Domain:

```
Transactio
```

Range:

```
Place
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies a place or places mentioned in a transaction. This does not include the place of transaction which is identified with the **has place of enactment** property.

#### has beneficiary (is beneficiary in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Testamentum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are named as a beneficiary of a **testamentum** transaction, that is, the beneficiary of a last will and testament. The beneficiary is named in the instructions of the testament and receives some form of bequest, usually an amount of money.

#### has buyer (is buyer in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Asecuratio
Venditio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the buyer or buyers named in a **venditio** (sales) or an **asecuratio** (insurance) transaction. This person is the indirect object of these transactions.

Examples:

The sale of an enslaved woman conducted 1484-05-29 where a certain Simone de Franchi sells an enslaved Circassian woman named Maria, who is approximately 30 years of age, to a certain Antonio de Zoalio, for 210 Genoese lire.

​	Target is the **Person** named “Antonio de Zoalio.”

#### has ceder (is ceder in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Cessio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are ceding their rights over some object in a **cessio** (a cession of rights) transaction. The ceder is the subject of the **cessio** transaction who transfers the object of the cession to a receiver.

#### has consenter (is provider of consent in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Transactio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies one or more persons attested as providing legal consent for one or more principal parties in a transaction. It is used in transactions where the transactors appear to be young or have not yet been emancipated and the father or guardian provides consent. It is also used in transactions involving women where the consent of two male relatives is required.

#### has date of transaction (is date of transaction)

Subproperty of:

```
P4 has time span
```

Domain:

```
Transactio
```

Range (Target):

```
Date
```

Quantification:

```
(0, n)
```

Scope note:

This property indicates the date of the transaction. It is an optional property, but it should be known in almost all cases. The property indicates the date or dates in YYYY-MM-DD format. If the month and day are unknown, then just enter the year in YYYY format. In transactions that occur over a series of discrete times (that is, whose contracts have with addenda entered on subsequent dates) enter the date or dates in chronological order. Do not enter date ranges for this item.

Examples:

The sale of an enslaved woman from 1466-03-13 in which the cutler named Battista de Merate sold an enslaved Circassian woman named Agnese, who was approximately 30 years of age, to a certain Juan Gracia, a citizen of Valencia, for 115 Genoese lire.

​	Target is the **Date** value “1466-03-13”

#### has debt holder (is debt holder in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Debitum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as debt holders in a **debitum** (acknowledgment of debt) transaction.

#### has debtor (is debtor in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Debitum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as the debtor in a **debitum** (acknowledgment of debt) transaction. The debtor is the subject of this transaction.

#### has defendant (is defendant in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Sententia
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as defendants in a **sententia** (a sentence or judgement) transaction. The defendant is the indirect object of these transactions who receives a sentence from the sentencer.

#### has delegator (is delegator in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Procura
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies a person or persons named as the delegators in a **procura** (procuration or power of attorney) transaction. The delegator is the subject of the **procura** transaction who names a person or persons to act as their procurator.

#### has description (describes)

Subproperty of:

```
P190 has symbolic content
```

Domains:

```
Asset
Nationality
Person
Place
Transactio
```

Range:

```
String
```

Quantification:

```
(0, 1)
```

Scope note:

The property refers to the textual description of an object in the ontology. For the description of a **transactio**, it should be precise and include information on the principal transactors, the objects of the transaction, and geographical locales related to the transaction.

Examples:

The sale of an enslaved woman recorded in the contract “Tommaso Duracino, filza 25, series I, nr. 122” can be described as follows:

> The slaveholder named Simone de Franchi sells an enslaved Circassian woman named Maria, who is approximately 30 years of age, to a certain Antonio de Zoalio, for 210 Genoese lire.

#### has donator (is donator in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Datio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as the gift givers in a **donatio** (a gift or donation) transaction (the *donator* from classical law). The field is optional but highly recommended for contextual purposes.

#### has executor (is executor in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Inventarium
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as the executor in an **inventarium** (an inventory of goods), generally for a recently deceased person. The executor is the subject of the **inventarium** transaction. This property differs from the **has named** executor in the **inventarium** transaction where the person or persons named as an executor are the objects of that transaction.

#### has geospatial location (is geospatial location for)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Place
```

Range:

```
an object in the geonames ontology
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the geospatial location of a place using the **geonames** ontology.

#### has gift (is gift in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Datio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects that are given in a **datio** (a gift or donation) transaction. They are the indirect objects of the donation and are generally **assets** of some sort. In the case of transactions related to the rights over enslaved persons, the object of donation can be a **person**.

#### has heir (is heir in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Testamentum
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are named as heirs of a **testamentum** transaction, that is, the heirs of a last will and testament. The heir is named in the instructions of the testament and receives some form of inheritance, usually assets of some sort.

#### has holder (is holder in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Locatio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the persons named in a **locatio** (lease) transaction who are conducting the lease, the so-called *locator* from classical law. The holder is the subject of the **locatio** transaction and is generally, but not always, the legal owner of the object of the lease (for example, in the case of a sub-lease). In the case of transactions related to the rights over enslaved persons, the holder can be a **person**.

#### has issuer of quittance (is issuer of quittance in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Quitatio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are issue the quittance in a **quitatio** (a quittance or discharge from obligations) transaction. This person is the subject of the **quitatio** transaction.

#### has item of bequest (is bequest in)

Subproperty of:

```
P105 right held by (has right on)
```

Domain:

```
Testamentum
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of named as bequests in a **testamentum** (a last will and testament) transaction. A bequest is generally an **asset** of some sort. In the case of bequests related to the rights over enslaved persons, the bequest can be a **person**.

#### has item of inheritance (is an item of inheritance in)

Subproperty of:

```
P105 right held by (has right on)
```

Domain:

```
Testamentum
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of named as items of inheritance in a **testamentum** (a last will and testament) transaction. An item of inheritance is generally an **asset** of some sort. In the case of inheritances related to the rights over enslaved persons, the inheritance can be a **person**.

#### has inquisitor (is inquisitor in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Testimonium
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as the inquisitors or examiners in a **testimonium** (a testimony under oath) transaction. This person is the indirect object of the contract who receives the object of testimony from the testifier.

#### has known date range of activity (is the known date range of activity of)

Subproperty of:

```
P4 has time span
```

Domain:

```
Person
```

Range:

```
Date
```

Quantification:

```
(0, 1)
```

Scope note:

This property indicates the known date range in which a historical person was known to be living. It is a date range specified in years, in the form of “YYYY–YYYY” (*terminus ante quem–terminus post quem*) or in the case where only one year is certain as “–YYYY” (–*terminus post quem*).

#### has location (is location of)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Inventarium
Place
```

Range:

```
Place
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the location of the objects named in an **inventarium** (an inventory of goods) transaction or the location of a **place** object within another **place** object.

#### has loconym (is loconym of)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Person
```

Range:

```
Place
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the place indicated by a **person** identified with a loconym. It does not necessarily imply current habitation or citizenship in that place.

#### has marriage to

Subproperty of:

```
P2 has type (is type of)
```

Domain:

```
Person
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies a historical **person** with whom another historical **person** has entered marriage.

#### has name (is name of)

Subproperty of:

```
P1 is identified by (identifies)
```

Domain:

```
Person
```

Range:

```
Text
```

Quantification:

```
(1, 1)
```

Scope note:

The normalized name of the person or place according to the naming conventions of the database. This is a required property. Refer to the *GEMENET Naming Conventions* document for details.

Examples:

The **Person** named as *Ieronimo de Carolo seatario Caroli cive Ianue* in the source.

​	Target is the **Text** item “Girolamo de Carlo”

The **Person** named as *Nicolao de Payrano textore pannorum septe Antonii cive Ianue* in the source.

​	Target is the **Text** item “Niccolò de Peirano”

#### has name from source (has normalized name)

Subproperty of:

```
P139 has alternative form
```

Domain:

```
Person
```

Range:

```
Text
```

Quantification:

```
(0, n)
```

Scope note:

The name of the **Person** exactly how they are described in the source material, with alternate spellings, languages, prefixes, and suffixes, and so on. There can be many instances of this property for a Person entity.

Examples:

The **Person** named as *Ieronimo de Carolo seatario Caroli cive Ianue* in the source.

​	Target is the **Text** item “Ieronimo de Carolo seatario Caroli cive Ianue.”

The **Person** named as *Nicolao de Payrano textore pannorum septe Antonii cive Ianue* in the source.

​	Target is the **Text** item “Nicolao de Payrano textore pannorum septe Antonii cive Ianue.”

#### has nationality (is nationality of)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Person
```

Range:

```
Nationality
```

Quantification:

```
(0, n)
```

Scope note:

This property the regional provenance of **Person** identified in the ontology.

#### has note (is note for)

Subproperty of:

```
P3 has note
```

Domain:

```
Asset
Nationality
Person
Place
Transactio
```

Range:

```
Text
```

Quantification:

```
(0, n)
```

Scope note:

This property refers to informal and non-public descriptions, administrative comments, and other textual data related to objects in the ontology.

#### has object of agreement (is object of agreement in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Acordatio
Compromissum
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects named in an **acordatio** (a mutual agreement) or a **compromissum** (a mutual agreement to abide by an arbitration). They are the direct objects of the agreement and are generally an **asset** of some sort. In the case of agreements regarding the rights over enslaved persons, the object of an agreement can be a **person**.

Examples:

An **acordatio famuli** conducted on 1455-02-17 in which a certain Maria de Byach, described as being from the Crimean Peninsula (*partium Sclavonie*) entered into an agreement with Battista Bonivento to work as a household servant for ten years.

​	Target is the **Person** named “Maria de Byach”.

#### has object of arbitration (is object of arbitration in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Arbitratio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects named in an **arbitratio** (arbitration) transaction. They are the direct objects of arbitration and are generally an **asset** of some sort. In the case of arbitrations regarding the rights over enslaved persons, the object of arbitration can be a **person**.

#### has object of cession (is object of cession in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Cessio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of cession named in a **cessio** (cession of rights) transaction. They are the direct objects of the transaction and are generally an **asset** of some sort. In the case of cessions related to the rights over enslaved persons, the object of cession can be a **person**.

#### has object of debt (is object of debt in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Debitum
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of debt named in a **debitum** (an acknowledgment of debt) transaction. They are the direct objects of the acknowledgment of debt. This is generally an **asset** of some sort. In the case of transactions related to the rights over enslaved persons, the object of debt can be a **person**.

#### has object of dowry (is object of dowry in)

Subproperty of:

```
has object of promise
```

Domain:

```
Dos
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of a dowry named in a **dos** (a promise of dowry) transaction. They are the direct objects of the promise of the dowry and are generally an **asset** of some sort. In the case of dowries related to the rights over enslaved persons, the object of dowry can be a **person**.

#### has object of insurance (is object of insurance in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Asecuratio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects named in an **asecuratio** (insurance) transaction. They are the direct objects of insurance and are generally an **asset** of some sort. In the case of insurance regarding the lives of enslaved pregnant women, or the life insurance on persons in general, the object of an insurance can be a **person**.

#### has object of inventory (is object of inventory in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Inventarium
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects listed in an **inventarium** (an inventory of goods) transaction. They are the indirect objects of the transaction and are generally an **asset** of some sort. In the case of inventories related to deceased slaveholders, the object of an inventory can be a **person**.

#### has object of lease (is object of lease in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Locatio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects of lease named in a **locatio** (a leasing) transaction. They are the direct objects of the lease and are generally an **asset** of some sort. In the case of sale regarding enslaved persons, the object of a lease can be a **person**.

#### has object of partnership (is object of partnership in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Societas
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects in a **societas** (a business partnership) transaction. They are the direct objects of the agreement and are generally an **asset** of some sort. In the case of partnerships regarding the rights over enslaved persons, the object of partnership can be a **person**.

#### has object of procuration (is object of procuration in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Procura
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects named in a **procura** (procuration or power of attorney) transaction. They are the indirect objects of the transaction and are generally an **asset** of some sort. In the case of procuration regarding the rights over the enslaved, the object of procuration can be a **person**. A substantial proportion of **procura** transactions are general procurations which do not indicate an object related to the transaction.

#### has object of promise (is object of promise in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Dos
Promissio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects of a **promissio** (a general promise) transaction. They are the direct objects of the promise of the dowry and are generally an **asset** of some sort. In the case of promises related to the rights over enslaved persons, the object of promise can be a **person**.

#### has object of quittance (is object of quittance in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Quitatio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects named in a **quitatio** (a quittance or release from obligation) transaction. They are the direct objects of the quittance and are generally an **asset** of some sort. In the case of quittances regarding enslaved persons, the object of a quittance can be a **person**.

#### has object of sale (is object of sale in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Venditio
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the objects of sale named in a **venditio** (a sales) transaction. They are the direct objects of sale and are generally an **asset** of some sort. In the case of sales regarding enslaved persons, the object of a sale can be a **person**.

#### has object of testimony (is object of testimony in)

Subproperty of:

```
P30 transferred custody of
```

Domain:

```
Testimonium
```

Range:

```
Asset
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the object or objects named in a **testimonium** (a testimony under oath) transaction. They are the direct objects of the testimony and are generally some information about an **asset** of some sort. In the case of testimony regarding the rights over enslaved persons, the object of testimony can be a **person**.

#### has parent (is parent of)

Subproperty of:

```
P152 has parent (is parent of)
```

Domain:

```
Person
```

Range:

```
Person
```

Quantification:

```
(0, 2)
```

Scope note:

This property identifies the historical person or persons who are the biological parent or parents of another historical person.

#### has partner (is partner of)

Subproperty of:

```
has additional participant
```

Domain:

```
Societas
```

Range:

```
Person
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the person or persons who agree to the terms of a **societas** (a business partnership) transaction. They are the subjects of the contract.

#### has party to agreement (is party to agreement in)

Subproperty of:

```
has participant
```

Domain:

```
Acordatio
Compromissum
```

Range:

```
Person
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the parties who agree to the terms of an **acordatio** (a mutual agreement) transaction or who agree to be bound to the decision of an arbitrator in a **compromissum** (a mutual agreement to abide by an arbitration) transaction. They are the subject of these types of contracts.

Examples:

The **compromissum** conducted on 1460-01-30 between Benedetto Ittaliano and the heirs of Catarina Imperiale, which are her sons Simone, Giacomo, and Gregorio Imperiale. The agreement relates to a dispute over the goods of the deceased Lanfranco Imperiale, the spouse of Catarina. Gandolfo de Fossato and Francesco Marchesio are named as arbitrators.

​	Target is the **Person** named “Gandolfo de Fossato”

​	Target is the **Person** named “Francesco Marchesio”

#### has party to arbitration (is party to arbitration in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Arbitratio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the party or parties to arbitration in an **arbitratio** (arbitration) transaction, that is, the party or parties for which the arbitration is being issued. They are the indirect object of the transaction.

#### has patrilineage (is patrilineage of)

Subproperty of:

```
P139 has alternative form
```

Domain:

```
Person
```

Range:

```
Text
```

Quantification:

```
(0, 1)
```

Scope note:

This property denotes a patrilineal identifier, or patronym, to allow for easier identification of the historical person. Keep it simple: do not include more than two patrilineal descendants. This property is primarily for administrators and advanced users and is used to make more precise searches.

Examples:

The person named *Ieronimo de Carolo seatario Caroli cive Ianue* in the source.

​	Target is the **Text** object “Girolamo de Carlo q. Carlo”

The person named *Nicolao de Payrano textore pannorum septe Antonii cive Ianue* in the source.

​	Target is the **Text** object “Niccolò de Peirano q. Antonio”

#### has place of burial (is object of burial in)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Testamentum
```

Range:

```
Place
Real Estate
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the place of burial named by the testator in a **testamentum** (last will and testament) transaction. It can be a general geographical place, like “the city of Genoa,” or a specific piece of real estate, like “the cloister of the Cathedral of San Lorenzo.”

#### has place of enactment (is place of enactment in)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Transactio
```

Range:

```
Place
Real Estate
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the place of enactment where the transaction was formalized. It can be a general geographical place, like “the city of Genoa,” or a specific piece of real estate, like “the house of Angelo and Ottobone di Negro.”

#### has place of origin (is place of origin for)

Subproperty of:

```
P89 falls within (contains)
```

Domain:

```
Nationality
```

Range:

```
Place
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the geographical place of origin in descriptions of **nationality**.

#### has plaintiff (is plaintiff in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Sententia
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as a plaintiff in a **sententia** (a sentence or judgement) transaction. The plaintiff is the indirect object of these transactions who receives a sentence from the sentencer.

#### has primary transactor (is primary transactor in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Cassatio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the original primary transactor or transactors named in a **cassatio** (annulment) transaction. These are the subject or subjects of the earlier transaction that is annulled by this transaction.

#### has procurator (is procurator in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Transactio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies one or more persons attested as procurators or general representatives for one or more principal parties in a transaction. It should not be used to identify the principal parties of a transaction; that is this property is not the same as the **has appointed procurator** property which identifies the indirect object of a **procura** (a procuration or power of attorney) transaction.

#### has promisor (is promisor in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Dos
Franchixia
Promissio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as the promisor (the one making a promise) in **dos** (a promise of dowry), **franchixia** (a manumission), and **promissio** (a promise) transactions. The promisor is the subject of the transaction.

#### has receiver (is receiver in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Cessio
Datio
Dos
Franchixia
Locatio
Promissio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons names as the receivers of the rights over an object in a **cessio** (a cession of rights), a **datio** (a donation), a **dos** (a promise of dowry), a **franchixia** (a manumission), a **locatio** (a lease) transaction, or a **promissio** (a promise) transaction. The receiver is the indirect object of the transaction.

#### has receiver of quittance (is receiver of quittance in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Quitatio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are receive a quittance, that is, a discharge from some form of obligation, in a **quitatio** transaction. This person is the indirect object of these transactions.

#### has recorder of inventory (is the recorder of inventory in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Inventarium
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons appointed by the executor to record the inventory in an **inventarium** (an inventory of goods) transaction. The **recorder of inventory** is the object of the **inventarium** transaction.

#### has reference to original transaction (is original transaction in)

Subproperty of:

```
has reference to transaction
```

Domain:

```
Cassatio
```

Range:

```
Transactio
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the earlier transaction or transactions which a **cassatio** (an annulment) transaction nullifies. Select the **transactio** (the transaction) that is to be replaced.

#### has reference to transaction (is referenced in)

Subproperty of:

```
P67 refers to (is referred to by)
```

Superproperty of:

```
has reference to original transaction
```

Domain:

```
Transactio
```

Range:

```
Transactio
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies previously enacted transaction or transactions.

#### has rights holder (is rights holder of)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Archival Item
Dos
```

Range:

```
Organization
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or organization named as the holder of rights over some object. It is used in cases where the rights holder is not the subject or object of a transaction. In a **dos** (a promise of dowry), the rights holder refers to the woman for whom the dowry is being promised. In an **archival item** the rights holder is the institution that holds legal rights over that item.

#### has secondary transactor (is secondary transactor in)

Subproperty of:

```
P22 transferred title to
```

Domain:

```
Cassatio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the original secondary transactors named in a **cassatio** (annulment) transaction, that is, the direct objects of the earlier transaction that is annulled by this transaction.

#### has seller (is seller in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Venditio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as a seller in a **venditio** (sales) transaction, the so-called *venditor* from classical law. The seller is the subject of the sales transaction who sells the object of sale to the buyer. In the case of sales regarding enslaved persons, the object of the sale can be a **person**.

Examples:

The sales of an enslaved woman by the slaveholder Simone de Franchis in the sale titled “Tommaso Duracino, filza 25, series I, nr. 122”:

​	Target is the **Person** named “Simone de Franchis.”

#### has sentencer (is sentencer in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Sententia
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as sentencers in a **sententia** (a sentence or judgment) transaction. The sentencer is the subject of the sales transaction who transfers the judgement to the receiver of the judgement.

#### has testator (is testator in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Testamentum
```

Range:

```
Person
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the person who is the testator of a **testamentum** transaction, that is, the person who is issuing their last will and testament. The testator is the subject of the contract.

#### has testifier (is testifier in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Testimonium
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as testifiers, that is, who provide testimony under oath, in a **testimonium** (a testimony under oath) transaction. The testifier is the subject of the transaction who transfers their testimony (the object of the testimony) to a questioner or inquisitor. In the case regarding enslaved persons, the object of the testimony can be a **person**.

#### has title (is title of)

Subproperty of:

```
P1 is identified by (identifies)
```

Domain:

```
Nationality
Place
Transactio
```

Range:

```
Title
```

Quantification:

```
(1, 1)
```

Scope note: 

This property identifies the title of an object. In the case of a **transactio**, the title follows a tightly prescribed format which should always be followed. It consists of the name of the notary who enacted the contract for the transaction, the enumeration of the contract in the archival fond according to the notary, the item number or folio number. See the examples below for proper naming examples.

Examples:

A **venditio** (sale) that is recorded in a contract contained in the fourth archival item assigned to Genoese notary Tommaso Duracino, a filza of loose contracts, with the enumeration number 177:

​	Target is the **Title** named “Tommaso Duracino, filza 4, nr. 177”.

A **locatio** (lease) that is recorded in a contract contained in the fifth archival item assigned to Genoese notary Tommaso Duracino, a filza of loose contracts, with the enumeration number 21 which had formerly been enumerated as number 338:

​	Target is the **Title** named “Tommaso Duracino, filza 5, nr. 21 (formerly nr. 338)”.

A **procura** (a procuration, power of attorney) that is recorded in a contract contained in the sixth archival item assigned to Genoese notary Tommaso Duracino, a filza with two series loose contracts, in the first series with the enumeration number 70:

​	Target is the **Title** named “Tommaso Duracino, filza 6, series I, nr. 70”.

A **venditio** (sale) that is recorded in a contract contained in the fourteenth archival item assigned to Genoese notary Benvenuto Bracelli, a single register of contracts dated 1375–1390, and located on folio 146v.

​	Target is the **Title** named “Benvenuto Bracelli, register 14, 1375–1390, fol. 146v”.

A **societas** (business partnership) that is recorded in a contract in the second archival item assigned to Genoese notary Giuliano Canella, with two registers, within the second volume dated 1410–1412 and located on folio 114r.

​	Target is the **Title** named “Giuliano Canella, register 2, volume II, 1410–1412, fol. 114r”.

#### has title from source (has normalized title)

Subproperty of:

```
P139 has alternative form
```

Domain:

```
Nationality
Place
```

Range:

```
Text
```

Quantification:

```
(0, n)
```

Scope note:

The title of an object exactly how they are described in the source material, with alternate spellings, languages, prefixes, and suffixes, and so on.

#### has type (is type)

Subproperty of:

```
P2 has type
```

Domain:

```
Transactio
```

Range:

```
Text
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the type of transaction—specified in Latin—and is optional. If the notary has assigned a specific title to this transaction, it should be entered here exactly as it was written. If it is a special type of transaction without a title given by the notary, then you may enter a title from a controlled vocabulary list. This field should be recorded Latin in order to organize the contract types.

Examples:

The sale of an enslaved woman with the title “Venditio sclave” written by the notary.

​	The target is the **Text** item “Venditio sclave” from the controlled vocabulary list.

The sale of a house with the with no title provided by the notary.

​	The target is the **Text** item “Venditio domus” from the controlled vocabulary list.

#### has underwriter (is underwriter in)

Subproperty of:

```
P23 transferred title from
```

Domain:

```
Asecuratio
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons named as underwriters in an **asecuratio** (insurance) transaction. The underwriter is the subject of the transaction.

Examples:

The insurance by Giovanni de Guisulfis against the risk of death from childbirth from the underwriter Cattaneo Grimaldi for an enslaved Russian woman named Lucia.

​	Target is the **Person** named “Cattaneo Grimaldi”

#### has unique identifier (is unique identifier for)

Subproperty of:

```
P48 has preferred identifier (is preferred identifier of)
```

Domain:

```
Asset
Nationality
Person
Place
Transactio
```

Range:

```
Identifier
```

Quantification:

```
(1, 1)
```

Scope note:

This property identifies the unique identifier for an object in the ontology. It should be entered as a UUID-4 format string.

#### has witness (is witness in)

Subproperty of:

```
P11 had participant
```

Domain:

```
Transactio 
```

Range:

```
Person
```

Quantification:

```
(0, n)
```

Scope note:

This property identifies the person or persons who are named witnesses in a transaction.

#### is enacted by (enacts)

Subproperty of:

```
P11 had participant
```

Domain:

```
Transactio 
```

Range:

```
Person
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the person responsible for enacting the transaction by recording it in a contractual object, who is always a notary. In some rare cases the notary named in the title of the contract that records the transaction, which comes from the archival item, may not be the same as the notary who enacted the transaction.

Examples:

The sale of an enslaved woman in the contract named “Martino Brignole, filza 3, nr. 73”:

​	Target is the **Person** named “Martino Brignole.”

The sale of an enslaved Crimean woman named Margarita in the contract named “Busta R bis 1, Ignoto Genova, nr. 132”, 

​	In this particular contract the notary is unknown, so the property does not apply.

#### is part of archival item (archival item contains)

Subproperty of:

```
P46 forms part of
```

Domain:

```
Transactio
```

 Range:

```
Archival Resource
```

Quantification:

```
(0, 1)
```

Scope note:

This property identifies the archival item that contains the record of the transaction. This will be the register, filza, or busta that contains the physical copy of the contract. The property identifies an item that already exists as an **Archival Resource** entity in the database beforehand. This property is optional but should be known in most cases.

Examples:

The sale of an enslaved woman with the title “Giovanni Danove, filza 2, series II, nr. 135”:

​	Target is the **Archival Resource** named “Notai antichi 917”.

------

[[1\]](#_ftnref1) On the CIDOC-CRM conceptual framework, see Martin Doerr *et al*, eds., “Definition of the CIDOC Conceptual Reference Model, Version 7.1.1” (CIDOC CRM Special Interest Group, 2021).