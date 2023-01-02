# ecomt

function DessertsList(props) {
  // Implement the component here.
  let data = props.data
  const result = data.filter(checkGreaterCalorie);

function checkGreaterCalorie(i) {
  return i.calories <500;
}
  const arr = result.sort(function(a,b){return a.calories-b.calories});
  const listItems = arr.map((item) =>
  <li>{`${item.name} - ${item.calories} cal `}</li> 
);


const sort = (data, sortKey) => sortKey ? [...data].sort((a, b) => a[sortKey] > b[sortKey]) : data

  
  return (<>
    <ul>
      {listItems}
    </ul>
  </>);
}

export default DessertsList;
