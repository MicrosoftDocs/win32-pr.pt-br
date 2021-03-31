---
title: Suporte de esquema
description: WsUtil.exe dá suporte ao esquema XSD especificado no esquema XML.
ms.assetid: 33096cda-9dbe-44d2-8d08-410bc33ae81c
keywords:
- Serviços Web de suporte de esquema para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dcf9d192c999333ee8b4e341e7722cd6bd59ff5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103917025"
---
# <a name="schema-support"></a><span data-ttu-id="886bc-106">Suporte de esquema</span><span class="sxs-lookup"><span data-stu-id="886bc-106">Schema support</span></span>

<span data-ttu-id="886bc-107">WsUtil.exe dá suporte ao esquema XSD especificado no [esquema XML](https://www.w3.org/XML/Schema).</span><span class="sxs-lookup"><span data-stu-id="886bc-107">WsUtil.exe supports the XSD schema specified at [XML Schema](https://www.w3.org/XML/Schema).</span></span> <span data-ttu-id="886bc-108">o arquivo XSD e o WSDL: Type devem ser tratados na mesma categoria, com a exceção em WSDL: Type quando um elemento global pode ser uma lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="886bc-108">xsd file and wsdl:type should be treated in the same category, with the exception in wsdl:type when a global element could be a parameter list.</span></span> <span data-ttu-id="886bc-109">Wsutil.exe gera descrições de elemento para todas as definições de elementos globais que podem ser usadas no serializador, com saída adicional para a estrutura de parâmetro especificada no [suporte a WSDL](wsdl-support.md).</span><span class="sxs-lookup"><span data-stu-id="886bc-109">Wsutil.exe generates element descriptions for all global element definitions that can be used in serializer, with additional output for parameter structure specified in [WSDL support](wsdl-support.md).</span></span>

## <a name="xsd-schema-support-level"></a><span data-ttu-id="886bc-110">Nível de suporte do esquema XSD</span><span class="sxs-lookup"><span data-stu-id="886bc-110">XSD Schema Support Level</span></span>

<span data-ttu-id="886bc-111">WsUtil.exe não dá suporte à extensão completa do esquema XSD.</span><span class="sxs-lookup"><span data-stu-id="886bc-111">WsUtil.exe does not support the full extent of XSD schema.</span></span> <span data-ttu-id="886bc-112">O nível de suporte atual é definido no [nível de suporte do esquema](schema-support-level.md).</span><span class="sxs-lookup"><span data-stu-id="886bc-112">The current support level is defined in [Schema support level](schema-support-level.md).</span></span>

<span data-ttu-id="886bc-113">Geração de identificador</span><span class="sxs-lookup"><span data-stu-id="886bc-113">Identifier generation</span></span>

<span data-ttu-id="886bc-114">O nome do elemento ou o nome do tipo no esquema pode não ser um identificador de C válido e os nomes são normalizados para nomes C válidos gerados.</span><span class="sxs-lookup"><span data-stu-id="886bc-114">Element name or type name in the schema might not be valid C identifier, and the names are normalized to generated valid C names.</span></span> <span data-ttu-id="886bc-115">Caracteres de identificador C inválidos são convertidos no nome Hex e um sublinhado ' \_ ' pode ser prefixado para o nome, se necessário.</span><span class="sxs-lookup"><span data-stu-id="886bc-115">Invalid C identifier characters are converted to the hex name, and a underscore '\_' might be prefixed to the name if necessary.</span></span> <span data-ttu-id="886bc-116">Os tipos anônimos são nomeados após o nome do elemento delimitador, mas prefixados com sublinhado " \_ " para evitar a colisão de nomes.</span><span class="sxs-lookup"><span data-stu-id="886bc-116">Anonymous types are named after the enclosing element name but prefixed with underscore "\_" to avoid name collision.</span></span> <span data-ttu-id="886bc-117">Os nomes de tipos globais são preservados, já que os caracteres inválidos são normalizados.</span><span class="sxs-lookup"><span data-stu-id="886bc-117">Global type names are preserved as it is after invalid characters are normalized.</span></span> <span data-ttu-id="886bc-118">Os tipos anônimos aninhados são prefixados com o nome do tipo pai.</span><span class="sxs-lookup"><span data-stu-id="886bc-118">Nested anonymous types are prefixed with the parent type name.</span></span>

<span data-ttu-id="886bc-119">Para cada definição de elemento global, wsutil.exe gera [**uma \_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) na estrutura de descrição global.</span><span class="sxs-lookup"><span data-stu-id="886bc-119">For every global element definition, wsutil.exe generates a [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) in the global description structure.</span></span> <span data-ttu-id="886bc-120">Para cada definição de tipo global, wsutil.exe gera uma descrição de tipo na estrutura de descrição global a ser referenciada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="886bc-120">For every global type definition, wsutil.exe generates a type description in the global description structure to be referenced by application.</span></span>

<span data-ttu-id="886bc-121">Para cada campo na estrutura, wsutil.exe gera uma [**Descrição de \_ campo \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) inserida como parte da estrutura do compartimento.</span><span class="sxs-lookup"><span data-stu-id="886bc-121">For each field in the structure, wsutil.exe generates a [**WS\_FIELD\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description) embedded as part of the enclosure structure.</span></span>

## <a name="simple-types"></a><span data-ttu-id="886bc-122">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="886bc-122">Simple Types</span></span>

<span data-ttu-id="886bc-123">Tipos de valor, conforme listado [**no \_ \_ tipo de valor WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), são tratados como tipos simples.</span><span class="sxs-lookup"><span data-stu-id="886bc-123">Value types, as listed in [**WS\_VALUE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type), are treated as simple types.</span></span> <span data-ttu-id="886bc-124">Observe que \_ o tipo de valor do WS \_ é realmente um subconjunto do [**\_ tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="886bc-124">Notice that WS\_VALUE\_TYPE is really a subset of [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="886bc-125">Ele inclui tipos de dados integral e float básicos, bem como DECIMAL, WS \_ DateTime e UUID.</span><span class="sxs-lookup"><span data-stu-id="886bc-125">It includes basic integral and float data types, as well as DECIMAL, WS\_DATETIME, and UUID.</span></span>

<span data-ttu-id="886bc-126">No modelo de serviço, em tipos simples são passados por valor, enquanto os tipos simples de out e in, out são passados por referência.</span><span class="sxs-lookup"><span data-stu-id="886bc-126">In service model, in simple types are passed by value, while out and in,out simple types are passed by reference.</span></span>

<span data-ttu-id="886bc-127">Wsutil crie uma descrição de elemento simples como abaixo para o elemento global que contém tipos simples.</span><span class="sxs-lookup"><span data-stu-id="886bc-127">Wsutil create simple element description like below for global element containing simple types.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="helloworld" type="xs:int"></xs:element>
</xs:schema>
```

<span data-ttu-id="886bc-128">Wsutil gera a descrição do elemento abaixo:</span><span class="sxs-lookup"><span data-stu-id="886bc-128">Wsutil generates the element description below:</span></span>

``` syntax
...  // global elements
{ // helloworld
{
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.helloworldTypeNamespace,
WS_INT32_TYPE,
0,
},
}, // helloworld
... 
```

<span data-ttu-id="886bc-129">Essa estrutura é gerada como parte da estrutura de descrição global gerada no arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="886bc-129">This structure is generated as part of the global description structure generated in header file:</span></span>

``` syntax
typedef struct _example_wsdl
{
WS_ELEMENT_DESCRIPTION helloworld;
} _example_wsdl;
```

## <a name="arrays"></a><span data-ttu-id="886bc-130">Matrizes</span><span class="sxs-lookup"><span data-stu-id="886bc-130">Arrays</span></span>

<span data-ttu-id="886bc-131">O elemento com maxOccurs maior que 1, ou sequência com apenas um item, e o elemento filho tem maxOccurs maior que 1, é tratado como matriz.</span><span class="sxs-lookup"><span data-stu-id="886bc-131">Element with maxOccurs larger than 1, or sequence with only one item, and the child element has maxOccurs larger than 1, is treated as array.</span></span> <span data-ttu-id="886bc-132">Para um elemento de matriz no esquema, wsutil.exe gera dois campos: um campo de contagem que não passa por fio e um campo de ponteiro contendo o tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="886bc-132">For an array element in schema, wsutil.exe generates two fields: one count field that does not go on wire, and one pointer field containing the array type.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleArray">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" maxOccurs="50" name="a" nillable="true" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="886bc-133">O arquivo de cabeçalho contém a definição de estrutura C para a matriz, com a conta de campo especificando a contagem da matriz.</span><span class="sxs-lookup"><span data-stu-id="886bc-133">Header file contains the C structure definition for the array, with field aCount specifying the count of the array.</span></span>

``` syntax
typedef struct SimpleArray
{
  unsigned int  aCount ;
  int  * a;
} SimpleArray;
```

<span data-ttu-id="886bc-134">A seguir, parte do protótipo LocalDefinition que descreve a matriz:</span><span class="sxs-lookup"><span data-stu-id="886bc-134">Following is part of the LocalDefinition prototype describing the array:</span></span>

``` syntax
... // globalElement part of the LocalDefinitions.
struct // SimpleArray
{
  struct // SimpleArray
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION * SimpleArrayFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArraydescs; // SimpleArray
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArray;

// Method with array parameters.
  typedef HRESULT (CALLBACK *SimpleMethodCallback)(
    const WS_OPERATION_CONTEXT* context,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);

  HRESULT CALLBACK SimpleMethod (
    WS_SERVICE_PROXY* serviceProxy,
    WS_HEAP* heap,
    unsigned int aCount,
    int* a,
    unsigned int *bCount,
    int** b,
    unsigned int* cCount,
    int** c,
    const WS_ASYNC_CONTEXT* asyncContext,
    WS_ERROR* error);
```

<span data-ttu-id="886bc-135">Veja a seguir as definições geradas das descrições acima, observe o \_ mapeamento de campo de elemento WS repetitivo \_ \_ \_ que indica o campo como um campo de matriz.</span><span class="sxs-lookup"><span data-stu-id="886bc-135">Following is the generated definitions of the above descriptions, notice the WS\_REPEATING\_ELEMENT\_FIELD\_MAPPING which indicates the field as an array field.</span></span>

``` syntax
...
{ // SimpleArray
  {   // SimpleArray
    { // field description for a
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      0,
      0,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArray, a),
      0,
      0,
      WsOffsetOf(SimpleArray, aCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },    // end of field description for a
    {    // fields description for SimpleArray
      (WS_FIELD_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.a,
    },
    {
      sizeof(SimpleArray),
      __alignof(SimpleArray),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.
      SimpleArrayFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.SimpleArrayFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    },   // struct description for SimpleArray
  },    // SimpleArray
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArray.SimpleArraydescs.structDesc,
  },
}, // SimpleArray
...
```

<span data-ttu-id="886bc-136">Se a matriz for um campo de parâmetro na mensagem de entrada/saída, haveria dois parâmetros reais gerados para o método.</span><span class="sxs-lookup"><span data-stu-id="886bc-136">If the array is a parameter field in input/output message, there would be two actual parameters generated for the method.</span></span> <span data-ttu-id="886bc-137">Se a matriz for um parâmetro out ou in out, haveria um nível adicional de indireção para ambos os campos em paramStruct.</span><span class="sxs-lookup"><span data-stu-id="886bc-137">If the array is an out or in,out parameter, there would be one additional level of indirection for both fields in paramStruct.</span></span>

## <a name="range-on-array"></a><span data-ttu-id="886bc-138">Intervalo na matriz</span><span class="sxs-lookup"><span data-stu-id="886bc-138">Range on Array</span></span>

<span data-ttu-id="886bc-139">Recomendamos a prática recomendada de não especificar maxOccur = "unbounded" para matrizes.</span><span class="sxs-lookup"><span data-stu-id="886bc-139">We recommend the best practice of not specifying maxOccur="unbounded" for arrays.</span></span> <span data-ttu-id="886bc-140">Em vez disso, um número inteiro fixo deve ser especificado para definir um limite superior de contagens de matriz permitidas.</span><span class="sxs-lookup"><span data-stu-id="886bc-140">Instead, a fixed integer number should be specified to set a upper bound of array counts allowed.</span></span> <span data-ttu-id="886bc-141">o intervalo tem suporte para tipos integrais, bem como cadeias de caracteres, matrizes de bytes e matrizes genéricas.</span><span class="sxs-lookup"><span data-stu-id="886bc-141">range is supported for integral types, as well as strings, byte arrays, and generic arrays.</span></span>

## <a name="heuristic-for-wrapped-as-opposed-to-unwrapped-array"></a><span data-ttu-id="886bc-142">Heurística para encapsulamento em oposição à matriz não encapsulada</span><span class="sxs-lookup"><span data-stu-id="886bc-142">Heuristic for Wrapped as Opposed to Unwrapped array</span></span>

<span data-ttu-id="886bc-143">Às vezes, as matrizes são encapsuladas dentro de outra estrutura para serem inseridas em uma estrutura de nível superior.</span><span class="sxs-lookup"><span data-stu-id="886bc-143">Sometimes arrays are wrapped inside another structure to be embedded in a top level structure.</span></span> <span data-ttu-id="886bc-144">Nesse caso, devemos remover a camada intermediária do wrapper.</span><span class="sxs-lookup"><span data-stu-id="886bc-144">In that case, we should remove the intermediate wrapper layer.</span></span> <span data-ttu-id="886bc-145">WsUtil.exe gera o mesmo protótipo e descrições que o SimpleArray descrito acima.</span><span class="sxs-lookup"><span data-stu-id="886bc-145">WsUtil.exe generates the same prototype and descriptions as SimpleArray described above.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="SimpleArray">
  <xs:sequence>
   <xs:element minOccurs="0" maxOccurs="50" name="aa" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="SimpleArrayWrapper">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="SimpleArray" type="tns:SimpleArray" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema>
```

<span data-ttu-id="886bc-146">Wsutil detecta que SimpleArrayWrapper é um wrapper em volta de SimpleArray e gera somente as seguintes estruturas, com estrutura separada para SimpleArray</span><span class="sxs-lookup"><span data-stu-id="886bc-146">Wsutil detects that SimpleArrayWrapper is a wrapper around SimpleArray, and generates following structures only, with separate structure for SimpleArray</span></span>

``` syntax
typedef struct SimpleArrayWrapper
{
  unsigned int  SimpleArrayCount ;
  int  * SimpleArray;
} SimpleArrayWrapper;

.. // global element inside the LocalDefinitions prototype
struct // SimpleArrayWrapper
{
  struct // SimpleArrayWrapper
  {
    WS_FIELD_DESCRIPTION SimpleArray;
    WS_FIELD_DESCRIPTION * SimpleArrayWrapperFields [1];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleArrayWrapperdescs; // SimpleArrayWrapper
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleArrayWrapper;
...
```

<span data-ttu-id="886bc-147">wsutil.exe gera as seguintes definições para o protótipo correspondente acima, observa que, na descrição do campo, os campos nome do wrapper e namespace do wrapper são preenchidos</span><span class="sxs-lookup"><span data-stu-id="886bc-147">wsutil.exe generates the following definitions for the matching prototype above, notices that in the field description, the wrapper name and wrapper namespace fields are filled in</span></span>

``` syntax
... // global element part of the LocalDefinitions structure:
{ // SimpleArrayWrapper
  {   // SimpleArrayWrapper
    { // WS_FIELD_DESCRIPTION  for SimpleArray
      WS_REPEATING_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArray),
      0,
      0,
      WsOffsetOf(SimpleArrayWrapper, SimpleArrayCount),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },    // end of field description for SimpleArray
    {    // array of field descriptions for SimpleArrayWrapper
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArray,
    },
    {  // WS_STRUCT_DESCRIPTION for SimpleArrayWrapper
      sizeof(SimpleArrayWrapper),
      __alignof(SimpleArrayWrapper),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.SimpleArrayWrapperFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    },   // struct description for SimpleArrayWrapper
    },    // SimpleArrayWrapper
  {  // WS_ELEMENT_DESCRIPTION for SimpleArrayWrapper
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayWrapperTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.SimpleArrayNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.SimpleArrayWrapper.SimpleArrayWrapperdescs.structDesc,
  },
}, // SimpleArrayWrapper
```

## <a name="structures"></a><span data-ttu-id="886bc-148">Estruturas</span><span class="sxs-lookup"><span data-stu-id="886bc-148">Structures</span></span>

<span data-ttu-id="886bc-149">Um complexType com vários elementos em uma sequência é uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="886bc-149">A complexType with multiple elements in a sequence is a structure.</span></span> <span data-ttu-id="886bc-150">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="886bc-150">For example,</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:complexType name="StructType">
  <xs:sequence>
   <xs:element minOccurs="0" name="FirstName" nillable="true" type="xs:string" />
   <xs:element minOccurs="0" name="LastName" nillable="true" type="xs:string" />
  </xs:sequence>
 </xs:complexType>
 <xs:element name="StructType" nillable="true" type="tns:StructType" />
</xs:schema>
```

<span data-ttu-id="886bc-151">Wsutil.exe gera um protótipo de estrutura como:</span><span class="sxs-lookup"><span data-stu-id="886bc-151">Wsutil.exe generates a structure prototype as:</span></span>

``` syntax
struct StructType
{
  WS_STRING FirstName;
  WS_STRING LastName;
};

// methods using structure parameters.
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  StructType* a,
  StructType** b,
  StructType** c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

<span data-ttu-id="886bc-152">o Wsutil gera o seguinte protótipo para LocalDefinition:</span><span class="sxs-lookup"><span data-stu-id="886bc-152">wsutil generates the following prototype for LocalDefinition:</span></span>

``` syntax
struct // StructType
{
  struct // StructType
  {
    WS_FIELD_DESCRIPTION FirstName;
    WS_FIELD_DESCRIPTION LastName;
    WS_FIELD_DESCRIPTION * StructTypeFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } StructTypedescs; // StructType
WS_ELEMENT_DESCRIPTION elementDesc;
}
```

<span data-ttu-id="886bc-153">A definição da estrutura é parecida com a mostrada abaixo, com duas descrições de campo na estrutura.</span><span class="sxs-lookup"><span data-stu-id="886bc-153">The definition for the structure looks like below, with two field descriptions in the structure.</span></span>

``` syntax
// global element inside LocalDefinitions.
{ // StructType
  {   // StructType
    { // field description for FirstName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, FirstName),
      0,
      0,
    },    // end of field description for FirstName
    { // field description for LastName
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.LastNameLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
      WS_STRING_TYPE,
      0,
      WsOffsetOf(StructType, LastName),
      0,
      0,
    },    // end of field description for LastName
    {    // fields description for StructType
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.FirstName,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.LastName,
    },
    { // WS_STRUCT_DESCRIPTION for StructType
      sizeof(StructType),
      __alignof(StructType),
      (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields,
      WsCountOf(example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.StructTypeFields),
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    },   // struct description for StructType
  },    // StructType
  {
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.StructTypeTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.FirstNameNamespace,
    WS_STRUCT_TYPE,
    (void *)&example_wsdlLocalDefinitions.globalElements.StructType.StructTypedescs.structDesc,
  },
}, // StructType
```

<span data-ttu-id="886bc-154">Para dar suporte à extensibilidade, as estruturas inseridas são sempre definidas passadas por referência.</span><span class="sxs-lookup"><span data-stu-id="886bc-154">To support extensibility, embedded structures are always defined passed by reference.</span></span> <span data-ttu-id="886bc-155">Em serviço, todas as estruturas out ou in, out são passadas por um ponteiro duplo para permitir a extensão futura da estrutura, bem como permitir a estrutura anulável.</span><span class="sxs-lookup"><span data-stu-id="886bc-155">In service, all out or in,out structures are passed by double pointer to allow future extension of the structure, as well as allowing nillable structure.</span></span>

## <a name="recursive-structures"></a><span data-ttu-id="886bc-156">Estruturas recursivas</span><span class="sxs-lookup"><span data-stu-id="886bc-156">Recursive Structures</span></span>

<span data-ttu-id="886bc-157">Há suporte para estruturas recursivas e os tipos inseridos são passados por referência.</span><span class="sxs-lookup"><span data-stu-id="886bc-157">Recursive structures are supported, and the embedded types is passed by reference.</span></span> <span data-ttu-id="886bc-158">Para o WSDL a seguir:</span><span class="sxs-lookup"><span data-stu-id="886bc-158">For the following wsdl:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="SimpleMethod">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="tns:example" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:complexType name="example">
  <xs:sequence>
   <xs:element minOccurs="0" name="d" type="tns:example" />
   <xs:element minOccurs="0" name="c" type="xs:int" />
  </xs:sequence>
 </xs:complexType>
</xs:schema>
```

<span data-ttu-id="886bc-159">O Wsutil gera as seguintes definições de tipo, bem como as descrições de tipo:</span><span class="sxs-lookup"><span data-stu-id="886bc-159">Wsutil generates the follow type definitions, as well as the type descriptions:</span></span>

``` syntax
typedef struct example
{
  struct example  * d;
  int32   c;
} example;

typedef struct SimpleMethod
{
  unsigned __int32   a;
  struct example  * b;
} SimpleMethod;

// global element part of the LocalDefinitions.
...
struct // SimpleMethod
{
  struct // SimpleMethod
  {
    WS_FIELD_DESCRIPTION a;
    struct // example
    {
      WS_FIELD_DESCRIPTION d;
      WS_FIELD_DESCRIPTION c;
      WS_FIELD_DESCRIPTION * exampleFields [2];
      WS_STRUCT_DESCRIPTION structDesc;
    } exampledescs; // example
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="886bc-160">A definição é gerada como abaixo:</span><span class="sxs-lookup"><span data-stu-id="886bc-160">The definition is generated as below:</span></span>

``` syntax
{   // SimpleMethod
  { // field description for a
    WS_ELEMENT_FIELD_MAPPING,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
    WS_INT32_TYPE,
    0,
    WsOffsetOf(SimpleMethod, a),
    0,
    0,
  },    // end of field description for a
  {   // example
    { // field description for d
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.dLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_STRUCT_TYPE,
      (WS_STRUCT_DESCRIPTION*)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.structDesc,
      WsOffsetOf(example, d),
      WS_FIELD_POINTER,
      0,
    },    // end of field description for d
    { // field description for c
      WS_ELEMENT_FIELD_MAPPING,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.cLocalName,
      (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
      WS_INT32_TYPE,
      0,
      WsOffsetOf(example, c),
      0,
      0,
    },    // end of field description for c
    {    // fields description for example
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.d,
      (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.c,
    },
  {
    sizeof(example),
    __alignof(example),
    (WS_FIELD_DESCRIPTION**)example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields,
    WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod.SimpleMethoddescs.exampledescs.exampleFields),
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.exampleTypeName,
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  },   // struct description for example
}
```

## <a name="structure-inheritence"></a><span data-ttu-id="886bc-161">Herança de estrutura</span><span class="sxs-lookup"><span data-stu-id="886bc-161">Structure inheritence</span></span>

<span data-ttu-id="886bc-162">Wsutil dá suporte à extensão de tipo complexo, em que um tipo complexo é uma extensão para outro tipo complexo.</span><span class="sxs-lookup"><span data-stu-id="886bc-162">wsutil supports complex type extension where one complex type is an extension to another complex type.</span></span>

``` syntax
<s:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:s="http://www.w3.org/2001/XMLSchema">
 <s:complexType name="LinkList">
  <s:sequence>
   <s:element minOccurs="0" name="d" type="tns:LinkList" />
   <s:element minOccurs="0" name="c" type="s:int" />
  </s:sequence>
 </s:complexType> 
 <s:element name="DerivedLinkList">
  <s:complexType>
   <s:complexContent>
    <s:extension base="tns:LinkList">
     <s:sequence>
      <s:element name="derive1" type="s:int" />
     </s:sequence>
    </s:extension>
   </s:complexContent>
  </s:complexType>
 </s:element>
</s:schema>
```

<span data-ttu-id="886bc-163">O fragmento XSD acima indica que DerivedLinkList deriva de linklist.</span><span class="sxs-lookup"><span data-stu-id="886bc-163">The above xsd fragment indicates that DerivedLinkList derives from LinkList.</span></span>

<span data-ttu-id="886bc-164">Wsutil.exe gera rotinas auxiliares para C e C++ para tornar mais fácil para o aplicativo configurar as informações de tipo de tipo base e tipos derivados.</span><span class="sxs-lookup"><span data-stu-id="886bc-164">Wsutil.exe generates helper routines for both C and C++ to make it easier for application to set up the type information of base type and derived types.</span></span> <span data-ttu-id="886bc-165">No código a seguir, \_ a \_ macro WS CPLUSPLUS é usada para diferenciar a definição da linguagem C e C++:</span><span class="sxs-lookup"><span data-stu-id="886bc-165">In the following code, \_WS\_CPLUSPLUS macro is used to differentiate definition for C and C++ language:</span></span>

``` syntax
#if defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  LinkList();
  LinkList(WS_STRUCT_DESCRIPTION*);
  struct _DerivedLinkList* WINAPI As_DerivedLinkList();
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct LinkList
{
  const struct _WS_STRUCT_DESCRIPTION* _type;
  struct LinkList * d;
  int  c;
} LinkList;

void WINAPI LinkList_Init(LinkList*);
#endif

#if defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList:LinkList
{
  _DerivedLinkList();
  int  derive1;
} _DerivedLinkList;
#endif

#if !defined(_WS_CPLUSPLUS)
typedef struct _DerivedLinkList
{
  struct LinkList _base;
  int  derive1;
} _DerivedLinkList;

struct _DerivedLinkList* WINAPI LinkList_As_DerivedLinkList(LinkList*);
#endif
```

<span data-ttu-id="886bc-166">No assistente de estilo C, antes de serialiation, o aplicativo chama a Wsutil \_ de link da rotina gerada como init para inicializar a estrutura e definir a descrição do tipo para a descrição do tipo de linklist.</span><span class="sxs-lookup"><span data-stu-id="886bc-166">In C style helper, before serialiation, application calls wsutil generated routine LinkList\_Init to initialize the structure and set the type description to LinkList type description.</span></span> <span data-ttu-id="886bc-167">Após a desserialização, o aplicativo pode chamar \_ a LinkId como \_ DerivedLinkList para obter o tipo derivado.</span><span class="sxs-lookup"><span data-stu-id="886bc-167">After deserialization, application can call LinkList\_As\_DerivedLinkList to get the derived type.</span></span>

<span data-ttu-id="886bc-168">Para recuperar informações de tipo em tempo de execução, Wsutil gera o primeiro campo de tipo base com o tipo de [**\_ \_ Descrição do WS struct**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description) e o mapeamento de campo de \* mapeamento de campo de [**\_ atributo de tipo \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) para descrever as informações de xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="886bc-168">To retrieve type information in runtime, wsutil generates the first field of base type with [**WS\_STRUCT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)\* type and [**WS\_TYPE\_ATTRIBUTE\_FIELD\_MAPPING**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping) field mapping to describe the xsi:type information.</span></span> <span data-ttu-id="886bc-169">O aplicativo pode definir diretamente ou verificar o campo para determinar o tipo real de estruturas.</span><span class="sxs-lookup"><span data-stu-id="886bc-169">Application can directly set or check the field to determine the actual type of structures.</span></span> <span data-ttu-id="886bc-170">Por exemplo, o código a seguir define o tipo da estrutura como DrivedLinkList:</span><span class="sxs-lookup"><span data-stu-id="886bc-170">For example, the following code set the type of the structure to be DrivedLinkList:</span></span>

``` syntax
_DerivedLinkList derivedLinkList;
derivedLinkList._base._type = (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription;
WsWriteType(
    writer,
    WS_ELEMENT_TYPE_MAPPING,
    WS_STRUCT_TYPE,
    (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription,
    ...);
```

<span data-ttu-id="886bc-171">Depois que a estrutura é desserializada, o aplicativo pode comparar diretamente a descrição do tipo para determinar o tipo desserializado:</span><span class="sxs-lookup"><span data-stu-id="886bc-171">After the structure is deserialized, application can directly compares the type description to determine the deserialized type:</span></span>

``` syntax
if (derviedLinkList._base._type == (WS_STRUCT_DESCRIPTION*)test_xsd.globalElements.DerivedLinkList.typeDescription)
{
    // the deserialized type is of type _DerivedLinkList
    ...
}
```

<span data-ttu-id="886bc-172">Wsutil gera a classe para a estrutura base e a estrutura derivada.</span><span class="sxs-lookup"><span data-stu-id="886bc-172">wsutil generate class for both base structure and derived structure.</span></span> <span data-ttu-id="886bc-173">O construtor padrão Inicializa o tipo e a descrição do tipo correspondente.</span><span class="sxs-lookup"><span data-stu-id="886bc-173">The default constructor initialize the type and matching type description.</span></span> <span data-ttu-id="886bc-174">A rotina asderivtype ajuda a fazer a conversão de tipo seguro entre os tipos.</span><span class="sxs-lookup"><span data-stu-id="886bc-174">The AsDerivedType routine helps to do safe type casting between types.</span></span>

``` syntax
  { // field description for typeOfLinkList
  WS_TYPE_ATTRIBUTE_FIELD_MAPPING,
  0,
  0,
  WS_DESCRIPTION_TYPE,
  0,
  WsOffsetOf(LinkList, typeOfLinkList),
  0,
  0,
  },    // end of field description for typeOfLinkList        ...
  {
  sizeof(LinkList),
  __alignof(LinkList),
  (WS_FIELD_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields,
WsCountOf(test_xsdLocalDefinitions.globalTypes.LinkListdescs.LinkListFields),
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeName,
(WS_XML_STRING*)&test_xsdLocalDefinitions.dictionary.xmlStrings.LinkListTypeNamespace,
0,
(WS_STRUCT_DESCRIPTION**)&test_xsdLocalDefinitions.globalTypes.LinkListdescs.SubTypes,
  1,
  },   // struct description for LinkList
```

## <a name="nillable"></a><span data-ttu-id="886bc-175">{1&gt;nillable&lt;1}</span><span class="sxs-lookup"><span data-stu-id="886bc-175">nillable</span></span>

<span data-ttu-id="886bc-176">Há suporte para o atributo anulável para cadeias de caracteres, structs e matrizes de bytes.</span><span class="sxs-lookup"><span data-stu-id="886bc-176">nillable attribute is supported for strings, structs, and byte arrays.</span></span> <span data-ttu-id="886bc-177">O \_ atributo anulável do campo WS \_ será adicionado a campos com atributo anulável.</span><span class="sxs-lookup"><span data-stu-id="886bc-177">WS\_FIELD\_NILLABLE attribute will be added to fields with nillable attribute.</span></span> <span data-ttu-id="886bc-178">O ponteiro será definido como **NULL** se um elemento for anulável.</span><span class="sxs-lookup"><span data-stu-id="886bc-178">The pointer will be set to **NULL** if an element is nillable.</span></span> <span data-ttu-id="886bc-179">Um campo anulável em uma estrutura é tratado como um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="886bc-179">A nillable field in a structure is treated as a pointer.</span></span> <span data-ttu-id="886bc-180">Uma estrutura de parâmetro com atributo anulável será passada por referência.</span><span class="sxs-lookup"><span data-stu-id="886bc-180">A parameter structure with nillable attribute will be passed by reference.</span></span>

## <a name="pointers"></a><span data-ttu-id="886bc-181">ponteiros</span><span class="sxs-lookup"><span data-stu-id="886bc-181">pointers</span></span>

<span data-ttu-id="886bc-182">O tipo de valor deve ser passado por valor ou por referência para parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="886bc-182">Value type must be passed by value or by reference for out parameters.</span></span> <span data-ttu-id="886bc-183">O ponteiro duplo não é permitido, exceto para apenas estruturas de saída.</span><span class="sxs-lookup"><span data-stu-id="886bc-183">Double pointer is not allowed except for out only structures.</span></span>

## <a name="parameterless"></a><span data-ttu-id="886bc-184">Construtor</span><span class="sxs-lookup"><span data-stu-id="886bc-184">Parameterless</span></span>

<span data-ttu-id="886bc-185">Lembre-se da nossa discussão anterior sobre o nome de "parâmetros" para a parte da mensagem.</span><span class="sxs-lookup"><span data-stu-id="886bc-185">Recall our prior discussion for the "parameters" name for the message part.</span></span> <span data-ttu-id="886bc-186">Se isso for especificado, tentaremos gerar um quadro combinado para a mensagem de entrada e saída para a operação de serviço resultante.</span><span class="sxs-lookup"><span data-stu-id="886bc-186">If this is specified we will attempt to generate a combined frame for input and output message for the resulting service operation.</span></span> <span data-ttu-id="886bc-187">Se isso não for especificado, a operação de serviço resultante conteria então conter mensagens de entrada e saída como structs como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="886bc-187">If this is not specified the resulting service operation would then contain input and output messages as structs as parameters.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Sapphire.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Sapphire.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="noparameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="886bc-188">Portanto, para nossa operação SimpleMethod, a assinatura para o serviço e o cliente se parecerá.</span><span class="sxs-lookup"><span data-stu-id="886bc-188">Thus for our SimpleMethod operation the signature for the service and the client will look like.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback)
  (const WS_OPERATION_CONTEXT* context,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);

HRESULT CALLBACK SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  WS_HEAP* heap,
  SimpleMethodRequest* inMessage,
  SimpleMethodResponse** outMessage,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="security"></a><span data-ttu-id="886bc-189">Segurança</span><span class="sxs-lookup"><span data-stu-id="886bc-189">Security</span></span>

<span data-ttu-id="886bc-190">Consulte a seção de segurança na [ferramenta do compilador Wsutil](wsutil-compiler-tool.md) , bem como a [serialização](serialization.md)</span><span class="sxs-lookup"><span data-stu-id="886bc-190">See security section in [Wsutil Compiler tool](wsutil-compiler-tool.md) as well as [Serialization](serialization.md)</span></span>

 

 




