```js

const people = [
  {
    name: {
      first: '',
      last: '',
      preferred: '' // this will override first name if utilized
    },
    contact: {
      phone: '',
      phoneWorks: true,
      details: ''
    },
    supportContacts: [
      {
        name: '',
        relation: '', // options?
        contact: {
          phone: '',
          phoneWorks: true,
          details: ''
        }
      }
    ],
    medical: {
      condition: '',
      medication: '',
      dosage: '',
      doctorContact: ''
    },
    confidential: {
      immigrationStatus: '',
      probationStatus: '',
      citizenship: '',
      priorsAndWarrants: ''
    }

  }
];


const incidents = [
  {
    datetime: Date.now(),
    incidentType: 'arrest',
    locationID: '',
    action: '1',
    description: '',
    status: '',
    personID: '1',
    evidence: [
    ]
  }
];

const actions = [

];

const locations = [

];

export {
  people,
  incidents,
  actions,
  locations
}


```
