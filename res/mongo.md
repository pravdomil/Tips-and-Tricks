<h1>MongoDB Cheat Sheet</h1>

<ul>
  <li>
    <b><a href="https://docs.mongodb.com/manual/reference/operator/query/">Query and Projection Operators</a></b>
    <ul>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-comparison/">Comparison</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/eq/">eq</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/gt/">gt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/gte/">gte</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/in/">in</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/lt/">lt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/lte/">lte</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/ne/">ne</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/nin/">nin</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-logical/">Logical</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/and/">and</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/not/">not</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/nor/">nor</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/or/">or</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-element/">Element</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/exists/">exists</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/type/">type</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-evaluation/">Evaluation</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/expr/">expr</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/jsonSchema/">jsonSchema</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/mod/">mod</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/regex/">regex</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/text/">text</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/where/">where</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-geospatial/">Geospatial</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/geoIntersects/">geoIntersects</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/geoWithin/">geoWithin</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/near/">near</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/nearSphere/">nearSphere</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/box/">box</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/center/">center</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/centerSphere/">centerSphere</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/geometry/">geometry</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/maxDistance/">maxDistance</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/minDistance/">minDistance</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/polygon/">polygon</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/uniqueDocs/">uniqueDocs</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-array/">Array</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/all/">all</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/elemMatch/">elemMatch</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/size/">size</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query-bitwise/">Bitwise</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/query/bitsAllClear/">bitsAllClear</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/bitsAllSet/">bitsAllSet</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/bitsAnyClear/">bitsAnyClear</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/query/bitsAnySet/">bitsAnySet</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/projection/">Projection</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/projection/positional/">$</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/projection/elemMatch/">elemMatch</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/projection/slice/">slice</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/query/comment/">comment</a>.
      </li>
    </ul>
  </li>
  <li>
    <b><a href="https://docs.mongodb.com/manual/reference/operator/query-modifier/">Query Modifiers</a></b>
    <ul>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/comment/">comment</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/explain/">explain</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/hint/">hint</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/max/">max</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/maxTimeMS/">maxTimeMS</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/min/">min</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/orderby/">orderby</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/query/">query</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/returnKey/">returnKey</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/showDiskLoc/">showDiskLoc</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/meta/natural/">natural</a>.
      </li>
    </ul>
  </li>
  <li>
    <b><a href="https://docs.mongodb.com/manual/reference/operator/update/">Update Operators</a></b>
    <ul>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/update-field/">Field</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/update/currentDate/">currentDate</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/inc/">inc</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/min/">min</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/max/">max</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/mul/">mul</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/rename/">rename</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/set/">set</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/setOnInsert/">setOnInsert</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/unset/">unset</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/update-array/">Array</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/update/positional/">$</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/positional-all/">$[]</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/positional-filtered/">$[&lt;identifier&gt;]</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/addToSet/">addToSet</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/pop/">pop</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/pull/">pull</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/push/">push</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/pullAll/">pullAll</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/each/">each</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/position/">position</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/slice/">slice</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/update/sort/">sort</a>.
      </li>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/update-bitwise/">Bitwise</a>:
        <a href="https://docs.mongodb.com/manual/reference/operator/update/bit/">bit</a>.
      </li>
    </ul>
  </li>
  <li>
    <b><a href="https://docs.mongodb.com/manual/reference/operator/aggregation-pipeline/">Aggregation Pipeline Stages</a></b>
    <ul>
      <li>
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/addFields/">addFields</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/bucket/">bucket</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/bucketAuto/">bucketAuto</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/collStats/">collStats</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/count/">count</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/currentOp/">currentOp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/facet/">facet</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/geoNear/">geoNear</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/graphLookup/">graphLookup</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/group/">group</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/indexStats/">indexStats</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/limit/">limit</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/listLocalSessions/">listLocalSessions</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/listSessions/">listSessions</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/lookup/">lookup</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/match/">match</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/merge/">merge</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/out/">out</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/planCacheStats/">planCacheStats</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/project/">project</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/redact/">redact</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceRoot/">replaceRoot</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceWith/">replaceWith</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sample/">sample</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/set/">set</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/skip/">skip</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sort/">sort</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sortByCount/">sortByCount</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unionWith/">unionWith</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unset/">unset</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unwind/">unwind</a>.
      </li>
    </ul>
  </li>
  <li>
    <b><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/">Aggregation Pipeline Operators</a></b>
    <ul>
      <li>
        Arithmetic:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/abs/">abs</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/add/">add</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/ceil/">ceil</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/divide/">divide</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/exp/">exp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/floor/">floor</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/ln/">ln</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/log/">log</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/log10/">log10</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/mod/">mod</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/multiply/">multiply</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/pow/">pow</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/round/">round</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sqrt/">sqrt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/subtract/">subtract</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/trunc/">trunc</a>.
      </li>
      <li>
        Array:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/arrayElemAt/">arrayElemAt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/arrayToObject/">arrayToObject</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/concatArrays/">concatArrays</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/filter/">filter</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/first-array-element/">first</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/in/">in</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/indexOfArray/">indexOfArray</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/isArray/">isArray</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/last-array-element/">last</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/map/">map</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/objectToArray/">objectToArray</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/range/">range</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/reduce/">reduce</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/reverseArray/">reverseArray</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/size/">size</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/slice/">slice</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/zip/">zip</a>.
      </li>
      <li>
        Boolean:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/and/">and</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/not/">not</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/or/">or</a>.
      </li>
      <li>
        Comparison:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/cmp/">cmp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/eq/">eq</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/gt/">gt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/gte/">gte</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/lt/">lt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/lte/">lte</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/ne/">ne</a>.
      </li>
      <li>
        Conditional:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/cond/">cond</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/ifNull/">ifNull</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/switch/">switch</a>.
      </li>
      <li>
        Custom Aggregation:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/accumulator/">accumulator</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/function/">function</a>.
      </li>
      <li>
        Data Size:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/binarySize/">binarySize</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/bsonSize/">bsonSize</a>.
      </li>
      <li>
        Date:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateFromParts/">dateFromParts</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateFromString/">dateFromString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateToParts/">dateToParts</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateToString/">dateToString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dayOfMonth/">dayOfMonth</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dayOfWeek/">dayOfWeek</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dayOfYear/">dayOfYear</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/hour/">hour</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/isoDayOfWeek/">isoDayOfWeek</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/isoWeek/">isoWeek</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/isoWeekYear/">isoWeekYear</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/millisecond/">millisecond</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/minute/">minute</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/month/">month</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/second/">second</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toDate/">toDate</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/week/">week</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/year/">year</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/add/">add</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/subtract/">subtract</a>.
      </li>
      <li>
        Literal:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/literal/">literal</a>.
      </li>
      <li>
        Object:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/mergeObjects/">mergeObjects</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/objectToArray/">objectToArray</a>.
      </li>
      <li>
        Set:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/allElementsTrue/">allElementsTrue</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/anyElementTrue/">anyElementTrue</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/setDifference/">setDifference</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/setEquals/">setEquals</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/setIntersection/">setIntersection</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/setIsSubset/">setIsSubset</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/setUnion/">setUnion</a>.
      </li>
      <li>
        String:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/concat/">concat</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateFromString/">dateFromString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/dateToString/">dateToString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/indexOfBytes/">indexOfBytes</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/indexOfCP/">indexOfCP</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/ltrim/">ltrim</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/regexFind/">regexFind</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/regexFindAll/">regexFindAll</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/regexMatch/">regexMatch</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceOne/">replaceOne</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceAll/">replaceAll</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/rtrim/">rtrim</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/split/">split</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/strLenBytes/">strLenBytes</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/strLenCP/">strLenCP</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/strcasecmp/">strcasecmp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/substrBytes/">substrBytes</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/substrCP/">substrCP</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/substrBytes/">substrBytes</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/substrCP/">substrCP</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toLower/">toLower</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toString/">toString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/trim/">trim</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toUpper/">toUpper</a>.
      </li>
      <li>
        Text:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/meta/">meta</a>.
      </li>
      <li>
        Trigonometry:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sin/">sin</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/cos/">cos</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/tan/">tan</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/asin/">asin</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/acos/">acos</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/atan/">atan</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/atan2/">atan2</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/asinh/">asinh</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/acosh/">acosh</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/atanh/">atanh</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/degreesToRadians/">degreesToRadians</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/radiansToDegrees/">radiansToDegrees</a>.
      </li>
      <li>
        Type:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/convert/">convert</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/isNumber/">isNumber</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toBool/">toBool</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toDate/">toDate</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toDecimal/">toDecimal</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toDouble/">toDouble</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toInt/">toInt</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toLong/">toLong</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toObjectId/">toObjectId</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/toString/">toString</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/type/">type</a>.
      </li>
      <li>
        Accumulators:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/group/">group</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/accumulator/">accumulator</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/addToSet/">addToSet</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/avg/">avg</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/first/">first</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/first-array-element/">first</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/last/">last</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/last-array-element/">last</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/max/">max</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/mergeObjects/">mergeObjects</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/min/">min</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/push/">push</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/stdDevPop/">stdDevPop</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/stdDevSamp/">stdDevSamp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sum/">sum</a>.
      </li>
      <li>
        Accumulators in Other Stages:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/group/">group</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/project/">project</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/addFields/">addFields</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/set/">set</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/avg/">avg</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/max/">max</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/min/">min</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/stdDevPop/">stdDevPop</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/stdDevSamp/">stdDevSamp</a>,
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sum/">sum</a>.
      </li>
      <li>
        Variable:
        <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/let/">let</a>.
      </li>
    </ul>
  </li>
</ul>

<h2>Aggregation Pipeline Stages</h2>

<h3>Queries</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/match/">$match</a>: {
  &lt;query&gt;
} }
</pre>
    </td>
    <td>
      Filters the documents to pass only the documents that match the specified condition(s) to the
      next pipeline stage.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/geoNear/">$geoNear</a>: {
  &lt;options&gt;
} }
</pre>
    </td>
    <td>
      Outputs documents in order of nearest to farthest from a specified point. Starting in version
      4.2, MongoDB removes the limit and num options for the $geoNear stage as well as the default
      limit of 100 documents. To limit the results of $geoNear, use the $geoNear stage with the
      $limit stage.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sample/">$sample</a>: {
  size: &lt;integer&gt;
} }
</pre>
    </td>
    <td>
      Randomly selects the specified number of documents from its input.
    </td>
  </tr>
</table>

<h3>Fields</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/project/">$project</a>: {
  &lt;specification(s)&gt;
} }
</pre>
    </td>
    <td>
      Passes along the documents with the requested fields to the next stage in the pipeline. The
      specified fields can be existing fields from the input documents or newly computed fields.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/set/">$set</a>/<a href="https://docs.mongodb.com/manual/reference/operator/aggregation/addFields/">$addFields</a>: {
  &lt;newField&gt;: &lt;expression&gt;,
  ...
} }
</pre>
    </td>
    <td>
      Adds new fields to documents. $set outputs documents that contain all existing fields from the
      input documents and newly added fields.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unset/">$unset</a>:
  &lt;field&gt;
}
</pre>
    </td>
    <td>
      Removes/excludes fields from documents.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unwind/">$unwind</a>:
  &lt;field&gt;
}
</pre>
    </td>
    <td>
      Deconstructs an array field from the input documents to output a document for each element.
      Each output document is the input document with the value of the array field replaced by the
      element.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceRoot/">$replaceRoot</a>: {
  newRoot: &lt;replacement&gt;
} }
</pre>
    </td>
    <td>
      Replaces the input document with the specified document. The operation replaces all existing
      fields in the input document, including the _id field. You can promote an existing embedded
      document to the top level, or create a new document for promotion (see example).
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/replaceWith/">$replaceWith</a>:
  &lt;replacement&gt;
}
</pre>
    </td>
    <td>
      Replaces the input document with the specified document. The operation replaces all existing
      fields in the input document, including the _id field. With $replaceWith, you can promote an
      embedded document to the top-level. You can also specify a new document as the replacement.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/redact/">$redact</a>:
  &lt;expression&gt;
}
</pre>
    </td>
    <td>
      Restricts the contents of the documents based on information stored in the documents
      themselves.
    </td>
  </tr>
</table>

<h3>Lookup</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/lookup/">$lookup</a>: {
  from: &lt;collection to join&gt;,
  localField: &lt;field&gt;,
  foreignField: &lt;field&gt;,
  as: &lt;output array field&gt;
   
  or
   
  from: &lt;collection to join&gt;,
  let: {
    &lt;var_1&gt;: &lt;expression&gt;,
    ...,
    &lt;var_n&gt;: &lt;expression&gt;
  },
  pipeline: [ &lt;pipeline to execute on the collection&gt; ],
  as: &lt;output array field&gt;
} }
</pre>
    </td>
    <td>
      Performs a left outer join to an unsharded collection in the same database to filter in
      documents from the “joined” collection for processing. To each input document, the $lookup
      stage adds a new array field whose elements are the matching documents from the “joined”
      collection. The $lookup stage passes these reshaped documents to the next stage.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/graphLookup/">$graphLookup</a>: {
  from: &lt;collection&gt;,
  startWith: &lt;expression&gt;,
  connectFromField: &lt;string&gt;,
  connectToField: &lt;string&gt;,
  as: &lt;string&gt;,
  maxDepth: &lt;number&gt;,
  depthField: &lt;string&gt;,
  restrictSearchWithMatch: &lt;document&gt;
} }
</pre>
    </td>
    <td>
      Performs a recursive search on a collection, with options for restricting the search by
      recursion depth and query filter.
    </td>
  </tr>
</table>

<h3>Paging</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sort/">$sort</a>: {
  &lt;field1&gt;: &lt;sort order&gt;,
  &lt;field2&gt;: &lt;sort order&gt;,
  ...
} }
</pre>
    </td>
    <td>
      Sorts all input documents and returns them to the pipeline in sorted order.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/skip/">$skip</a>:
  &lt;integer&gt;
}
</pre>
    </td>
    <td>
      Skips over the specified number of documents that pass into the stage and passes the remaining
      documents to the next stage in the pipeline.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/limit/">$limit</a>:
  &lt;integer&gt;
}
</pre>
    </td>
    <td>
      Limits the number of documents passed to the next stage in the pipeline.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/count/">$count</a>:
  &lt;output field&gt;
}
</pre>
    </td>
    <td>
      Passes a document to the next stage that contains a count of the number of documents input to
      the stage.
    </td>
  </tr>
</table>

<h3>Grouping</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/group/">$group</a>: {
  _id: &lt;expression&gt;,
  &lt;field1&gt;: { &lt;accumulator1&gt; : &lt;expression1&gt; },
  ...
} }
</pre>
    </td>
    <td>
      Groups input documents by the specified _id expression and for each distinct grouping, outputs
      a document. The _id field of each output document contains the unique group by value. The
      output documents can also contain computed fields that hold the values of some accumulator
      expression. $group does not order its output documents.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/sortByCount/">$sortByCount</a>:
  &lt;expression&gt;
}
</pre>
    </td>
    <td>
      Groups incoming documents based on the value of a specified expression, then computes the
      count of documents in each distinct group.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/bucket/">$bucket</a>: {
  groupBy: &lt;expression&gt;,
  boundaries: [ &lt;lowerbound1&gt;, ... ],
  default: &lt;literal&gt;,
  output: {
    &lt;output1&gt;: { &lt;$accumulator expression&gt; },
    ...
    &lt;outputN&gt;: { &lt;$accumulator expression&gt; }
  }
} }
</pre>
    </td>
    <td>
      Categorizes incoming documents into groups, called buckets, based on a specified expression
      and bucket boundaries and outputs a document per each bucket. Each output document contains an
      _id field whose value specifies the inclusive lower bound of the bucket. The output option
      specifies the fields included in each output document.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/bucketAuto/">$bucketAuto</a>: {
  groupBy: &lt;expression&gt;,
  buckets: &lt;number&gt;,
  output: {
    &lt;output1&gt;: { &lt;$accumulator expression&gt; },
    ...
  }
  granularity: &lt;string&gt;
} }
</pre>
    </td>
    <td>
      Categorizes incoming documents into a specific number of groups, called buckets, based on a
      specified expression. Bucket boundaries are automatically determined in an attempt to evenly
      distribute the documents into the specified number of buckets.
    </td>
  </tr>
</table>

<h3>Pipelines</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/facet/">$facet</a>: {
  &lt;outputField1&gt;: [ &lt;stage1&gt;, &lt;stage2&gt;, ... ],
  &lt;outputField2&gt;: [ &lt;stage1&gt;, &lt;stage2&gt;, ... ],
  ...
} }
</pre>
    </td>
    <td>
      Processes multiple aggregation pipelines within a single stage on the same set of input
      documents. Each sub-pipeline has its own field in the output document where its results are
      stored as an array of documents.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unionWith/">$unionWith</a>: {
  coll: &lt;collection&gt;,
  pipeline: [ &lt;stage1&gt;, ... ]
} }
</pre>
    </td>
    <td>
      Performs a union of two collections; i.e. $unionWith combines pipeline results from two
      collections into a single result set. The stage outputs the combined result set (including
      duplicates) to the next stage.
    </td>
  </tr>
</table>

<h3>Collections</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/merge/">$merge</a>: {
  into:
    &lt;collection&gt; or
    { db: &lt;db&gt;, coll: &lt;collection&gt; },
  on:
    &lt;identifier field&gt; or
    [ &lt;identifier field1&gt;, ...],
  let: &lt;variables&gt;,
  whenMatched:
    &lt;replace|keepExisting|merge|fail|pipeline&gt;,
  whenNotMatched:
    &lt;insert|discard|fail&gt;
} }
</pre>
    </td>
    <td>
      Writes the results of the aggregation pipeline to a specified collection. The $merge operator
      must be the last stage in the pipeline.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/out/">$out</a>: {
  db: &lt;output-db&gt;,
  coll: &lt;output-collection&gt;
} }
</pre>
    </td>
    <td>
      Takes the documents returned by the aggregation pipeline and writes them to a specified
      collection. Starting in MongoDB 4.4, you can specify the output database. The $out stage must
      be the last stage in the pipeline. The $out operator lets the aggregation framework return
      result sets of any size.
    </td>
  </tr>
</table>

<h3>Debugging</h3>
<table>
  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/collStats/">$collStats</a>: {
  latencyStats: { histograms: &lt;boolean&gt; },
  storageStats: { scale: &lt;number&gt; },
  count: {},
  queryExecStats: {}
} }
</pre>
    </td>
    <td>
      Returns statistics regarding a collection or view.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/indexStats/">$indexStats</a>:
  {}
}
</pre>
    </td>
    <td>
      Returns statistics regarding the use of each index for the collection. If running with access
      control, the user must have privileges that include indexStats action.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/planCacheStats/">$planCacheStats</a>:
  {}
}
</pre>
    </td>
    <td>
      Returns plan cache information for a collection. The stage returns a document for each plan
      cache entry.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/currentOp/">$currentOp</a>: {
  allUsers: &lt;boolean&gt;,
  idleConnections: &lt;boolean&gt;,
  idleCursors: &lt;boolean&gt;,
  idleSessions: &lt;boolean&gt;,
  localOps: &lt;boolean&gt;
} }
</pre>
    </td>
    <td>
      Returns a stream of documents containing information on active and/or dormant operations as
      well as inactive sessions that are holding locks as part of a transaction. The stage returns a
      document for each operation or session. To run $currentOp, use the db.aggregate() helper on
      the admin database.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/listLocalSessions/">$listLocalSessions</a>:
  &lt;document&gt;
}
</pre>
    </td>
    <td>
      Lists the sessions cached in memory by the mongod or mongos instance.
    </td>
  </tr>

  <tr>
    <td>
      <pre>
{ <a href="https://docs.mongodb.com/manual/reference/operator/aggregation/listSessions/">$listSessions</a>:
  &lt;document&gt;
}
</pre>
    </td>
    <td>
      Lists all sessions stored in the system.sessions collection in the config database. These
      sessions are visible to all members of the MongoDB deployment.
    </td>
  </tr>
</table>
