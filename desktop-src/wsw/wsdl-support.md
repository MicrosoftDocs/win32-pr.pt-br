---
title: Contratos de serviço e WSDL
description: O utilitário Wsutil.exe gera um stub de linguagem C de acordo com os metadados WSDL fornecidos, bem como definições e descrições de tipo de dados para tipos de dados descritos por esquemas XML criados pelo usuário.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Suporte a WSDL
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19661e487c1a0dde871333376336bede239f9825
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642984"
---
# <a name="wsdl-and-service-contracts"></a><span data-ttu-id="d5176-106">Contratos de serviço e WSDL</span><span class="sxs-lookup"><span data-stu-id="d5176-106">WSDL and Service Contracts</span></span>

<span data-ttu-id="d5176-107">O utilitário [Wsutil.exe](web-service-compiler-tool.md) gera um stub de linguagem C de acordo com os metadados WSDL fornecidos, bem como definições e descrições de tipo de dados para tipos de dados descritos por esquemas XML criados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d5176-107">The [Wsutil.exe](web-service-compiler-tool.md) utility generates a C language stub according to supplied WSDL metadata, as well as data type definitions and descriptions for data types described by user-authored XML schemas.</span></span>


<span data-ttu-id="d5176-108">Este é um exemplo de documento WSDL e esquema XML que serve como base para a discussão a seguir:</span><span class="sxs-lookup"><span data-stu-id="d5176-108">The following is an example WSDL document and XML schema that serves as a basis for the discussion that follows:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:int" />
      <xs:element name="b" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:int" />
      <xs:element name="c" type="xs:int" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

<span data-ttu-id="d5176-109">Este exemplo fornece um contrato, ISimpleService, com um único método, SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="d5176-109">This example provides a contract, ISimpleService, with a single method, SimpleMethod.</span></span> <span data-ttu-id="d5176-110">"SimpleMethod" tem dois parâmetros de entrada do tipo **inteiro**, *a* e *b*, que são enviados do cliente para o serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-110">"SimpleMethod" has two input parameters of type **integer**, *a* and *b*, that are sent from the client to the service.</span></span> <span data-ttu-id="d5176-111">Da mesma forma, SimpleMethod tem dois parâmetros de saída do tipo **inteiro**, *b* e *c*, que são retornados ao cliente após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5176-111">Likewise, SimpleMethod has two output parameters of type **integer**, *b* and *c*, which are returned to the client after successful completion.</span></span> <span data-ttu-id="d5176-112">Na sintaxe C anotada por SAL, a definição do método aparece da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5176-112">In SAL-annotated C syntax, the method definition appears as follows:</span></span>

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

<span data-ttu-id="d5176-113">Nessa definição, ISimpleService é um contrato de serviço com uma única operação de serviço: SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="d5176-113">In this definition, ISimpleService is a service contract with a single service operation: SimpleMethod.</span></span>

<span data-ttu-id="d5176-114">O arquivo de cabeçalho de saída contém definições e descrições para referência externa.</span><span class="sxs-lookup"><span data-stu-id="d5176-114">The output header file contains definitions and descriptions for external reference.</span></span> <span data-ttu-id="d5176-115">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="d5176-115">This includes:</span></span>

-   <span data-ttu-id="d5176-116">Definições de estrutura C para tipos de elementos globais.</span><span class="sxs-lookup"><span data-stu-id="d5176-116">C structure definitions for global element types.</span></span>
-   <span data-ttu-id="d5176-117">Um protótipo de operação conforme definido no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-117">An operation prototype as defined in current file.</span></span>
-   <span data-ttu-id="d5176-118">Um protótipo de tabela de função para os contratos especificados no arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="d5176-118">A function table prototype for the contracts specified in the WSDL file.</span></span>
-   <span data-ttu-id="d5176-119">Protótipos de cliente e de proxy de serviço para todas as funções especificadas no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-119">Client proxy and service stub prototypes for all the functions specified in current file.</span></span>
-   <span data-ttu-id="d5176-120">Uma estrutura de dados de [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) para os elementos do esquema global definidos no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-120">A [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) data structure for the global schema elements defined in current file.</span></span>
-   <span data-ttu-id="d5176-121">Uma estrutura de dados de [**\_ \_ Descrição de mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para todas as mensagens especificadas no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-121">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) data structure for all the messages specified in current file.</span></span>
-   <span data-ttu-id="d5176-122">Uma estrutura de dados de [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para todos os contratos especificados no arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-122">A [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) data structure for all the contracts specified in current file.</span></span>

<span data-ttu-id="d5176-123">Uma estrutura global é gerada para encapsular todas as descrições globais dos tipos de esquema e tipos de modelo de serviço aos quais o aplicativo pode se referir.</span><span class="sxs-lookup"><span data-stu-id="d5176-123">One global structure is generated to encapsulate all the global descriptions for the schema types and service model types to which the application can refer.</span></span> <span data-ttu-id="d5176-124">A estrutura é nomeada usando um nome de arquivo normalizado.</span><span class="sxs-lookup"><span data-stu-id="d5176-124">The structure is named using a normalized file name.</span></span> <span data-ttu-id="d5176-125">Neste exemplo, Wsutil.exe gera uma estrutura de definições globais denominada "exemplo \_ WSDL" que contém todas as descrições do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="d5176-125">In this example, Wsutil.exe generates a global definitions structure named "example\_wsdl" that contains all the web service descriptions.</span></span> <span data-ttu-id="d5176-126">A definição de estrutura é gerada no arquivo de stub.</span><span class="sxs-lookup"><span data-stu-id="d5176-126">The structure definition is generated in the stub file.</span></span>

``` syntax
typedef struct _example_wsdl
{
  struct {
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    WS_ELEMENT_DESCRIPTION SimpleMethodResponse;
  } elements;
  struct {
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
    WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
  } messages;
  struct {
    WS_CONTRACT_DESCRIPTION DefaultBinding_ISimpleService;
  } contracts;
} _example_wsdl;

extern const _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="d5176-127">Para definições de elementos globais no documento de esquema XML (XSD), um protótipo de [**\_ \_ Descrição de elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , bem como a definição de tipo C correspondente, são gerados para cada um dos elementos.</span><span class="sxs-lookup"><span data-stu-id="d5176-127">For global element definitions in the XML schema document (XSD), one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) prototype, as well as the corresponding C type definition, are generated for each of the elements.</span></span> <span data-ttu-id="d5176-128">Os protótipos para as descrições de elemento para SimpleMethod e SimpleMethodResponse são gerados como membros na estrutura acima.</span><span class="sxs-lookup"><span data-stu-id="d5176-128">The prototypes for the element descriptions for SimpleMethod and SimpleMethodResponse are generated as members in the structure above.</span></span> <span data-ttu-id="d5176-129">As estruturas C são geradas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5176-129">The C structures are generated as follows:</span></span>

``` syntax
typedef struct SimpleMethod
{
  int   a;
  int   b;
} SimpleMethod;

typedef struct SimpleMethodResponse
{
  int   b;
  int   c;
} SimpleMethodResponse;
```

<span data-ttu-id="d5176-130">Da mesma forma, para tipos complexos globais, Wsutil.exe gera definições de estrutura C, como acima, sem as descrições de elemento correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d5176-130">Similarly for global complex types, Wsutil.exe generates type C structure definitions like above, without matching element descriptions.</span></span>

<span data-ttu-id="d5176-131">Para entrada WSDL, Wsutil.exe gera os seguintes protótipos e definições:</span><span class="sxs-lookup"><span data-stu-id="d5176-131">For WSDL input, Wsutil.exe generates the following prototypes and definitions:</span></span>

-   <span data-ttu-id="d5176-132">Um protótipo de [**\_ \_ Descrição de mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) é gerado para a descrição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-132">A [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) prototype is generated for the message description.</span></span> <span data-ttu-id="d5176-133">Essa descrição pode ser usada pelo modelo de serviço, bem como pela camada de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-133">This description can be used by the service model as well as the message layer.</span></span> <span data-ttu-id="d5176-134">Estruturas de descrição de mensagem são campos denominados "" na estrutura global.</span><span class="sxs-lookup"><span data-stu-id="d5176-134">Message description structures are fields named "messagename" in the global structure.</span></span> <span data-ttu-id="d5176-135">Neste exemplo, a descrição da mensagem é gerada como o \_ campo ISimpleService SimpleMethod \_ InputMessage na estrutura ISimpleService \_ SimpleMethod \_ InputMessage conforme especificado no arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="d5176-135">In this example, the message description is generated as the ISimpleService\_SimpleMethod\_InputMessage field in the ISimpleService\_SimpleMethod\_InputMessage structure as specified in the WSDL file.</span></span>
-   <span data-ttu-id="d5176-136">[**WS \_ O \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) protótipo de descrição do contrato é gerado para a descrição do contrato.</span><span class="sxs-lookup"><span data-stu-id="d5176-136">[**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) prototype is generated for the contract description.</span></span> <span data-ttu-id="d5176-137">Essa descrição é usada pelo modelo de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-137">This description is used by service model.</span></span> <span data-ttu-id="d5176-138">Estruturas de descrição de contrato são campos nomeados "contratados" na estrutura global.</span><span class="sxs-lookup"><span data-stu-id="d5176-138">Contract description structures are fields named "contractname" in the global structure.</span></span> <span data-ttu-id="d5176-139">Neste exemplo, a descrição do contrato é gerada como o campo padrão \_ ISimpleService na estrutura "WSDL de \_ exemplo \_ ".</span><span class="sxs-lookup"><span data-stu-id="d5176-139">In this example, the contract description is generated as the DefaultBinding\_ISimpleService field in the structure "\_example\_wsdl".</span></span>

<span data-ttu-id="d5176-140">As especificações de operação e tipo são comuns ao proxy e ao stub, e são geradas em ambos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="d5176-140">Operation and type specifications are common to both proxy and stub and they are generated in both files.</span></span> <span data-ttu-id="d5176-141">Wsutil.exe gerará uma cópia somente se o proxy e o stub forem gerados no mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5176-141">Wsutil.exe generates one copy only if both the proxy and stub are generated in the same file.</span></span>

## <a name="identifier-generation"></a><span data-ttu-id="d5176-142">Geração de identificador</span><span class="sxs-lookup"><span data-stu-id="d5176-142">Identifier generation</span></span>

<span data-ttu-id="d5176-143">As estruturas C geradas automaticamente listadas acima são criadas com base no nome especificado no arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="d5176-143">The autogenerated C structures listed above are created based on the name specified in WSDL file.</span></span> <span data-ttu-id="d5176-144">Um NCName XML não é comumente considerado um identificador C válido e os nomes são normalizados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d5176-144">An XML NCName is not commonly considered a valid C identifier, and the names are normalized as needed.</span></span> <span data-ttu-id="d5176-145">Os valores hexadecimais não são convertidos, e letras comuns, como ': ', '/' e '. ', são convertidas no caractere de sublinhado ' \_ ' para melhorar a legibilidade.</span><span class="sxs-lookup"><span data-stu-id="d5176-145">Hex values are not converted, and common letters like ':', '/' and '.' are converted to the underscore '\_' character to improve readability.</span></span>

## <a name="header-for-the-stub"></a><span data-ttu-id="d5176-146">Cabeçalho do stub</span><span class="sxs-lookup"><span data-stu-id="d5176-146">Header for the stub</span></span>

<span data-ttu-id="d5176-147">Para cada operação no contrato de serviço, uma rotina de retorno de chamada denominada "retorno de chamada <operationname> " é gerada.</span><span class="sxs-lookup"><span data-stu-id="d5176-147">For each operation in the service contract, one callback routine named "<operationname>Callback" is generated.</span></span> <span data-ttu-id="d5176-148">(Por exemplo, a operação "SimpleMethod" no contrato de serviço de exemplo tem um retorno de chamada gerado chamado "SimpleMethodCallback".)</span><span class="sxs-lookup"><span data-stu-id="d5176-148">(For example, the operation "SimpleMethod" in the example service contract has a generated callback named "SimpleMethodCallback".)</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

<span data-ttu-id="d5176-149">Para cada Wsutil.exe **PORTTYPE** WSDL gera uma tabela de função representando **PortType**.</span><span class="sxs-lookup"><span data-stu-id="d5176-149">For each WSDL **portType** Wsutil.exe generates a function table representing **portType**.</span></span> <span data-ttu-id="d5176-150">Cada operação em **PortType** tem um ponteiro de função correspondente para o retorno de chamada presente na tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="d5176-150">Each operation on the **portType** has a corresponding function pointer to the callback present in the function table.</span></span>

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

<span data-ttu-id="d5176-151">Protótipos de proxy são gerados para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="d5176-151">Proxy prototypes are generated for all operations.</span></span> <span data-ttu-id="d5176-152">O nome do protótipo é o nome da operação (nesse caso, "SimpleMethod") especificado no arquivo WSDL para o contrato de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-152">The prototype name is the operation name (in this case, "SimpleMethod") specified in WSDL file for the service contract.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a><span data-ttu-id="d5176-153">Geração de protótipo de descrição somente local</span><span class="sxs-lookup"><span data-stu-id="d5176-153">Local-only Description Prototype Generation</span></span>

<span data-ttu-id="d5176-154">Os arquivos de andstub de proxy contêm a definição para a estrutura de definições globais, incluindo protótipos e definições para as estruturas que contêm descrições somente locais e implementações de stub de serviço/proxy de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5176-154">The proxy andstub files contain the definition for the global definitions structure, including prototypes and definitions for the structures containing local-only descriptions and client proxy/service stub implementations.</span></span>

<span data-ttu-id="d5176-155">Todos os protótipos e definições locais para o arquivo stub são gerados como parte de uma estrutura de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="d5176-155">All prototypes and definitions that are local to the stub file are generated as part of an encapsulating structure.</span></span> <span data-ttu-id="d5176-156">Essa estrutura de descrição local abrangente fornece uma hierarquia clara das descrições exigidas pela camada de serialização e o modelo de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-156">This overarching local description structure provides a clear hierarchy of the descriptions required by the serialization layer and the service model.</span></span> <span data-ttu-id="d5176-157">A estrutura de descrição local tem protótipos semelhantes aos mostrados abaixo:</span><span class="sxs-lookup"><span data-stu-id="d5176-157">The local description structure has prototypes similar to the one shown below:</span></span>

``` syntax
struct _filenameLocalDefinitions
{
  struct {
  // schema related output for all the embedded 
  // descriptions that needs to describe global complex types.
  } globalTypes;
  // global elements.
  struct {
  // schema related output, like field description
  // structure description, element description etc.
  ...
  } globalElements;
  struct {
  // messages and related descriptions
  } messages;
  struct {
  // contract and related descriptions.
  } contracts;
  struct {
  // XML dictionary entries.
  } dictionary;
} _filenameLocalDefinitions;
```

## <a name="referencing-definitions-from-other-files"></a><span data-ttu-id="d5176-158">Referenciando definições de outros arquivos</span><span class="sxs-lookup"><span data-stu-id="d5176-158">Referencing definitions from other files</span></span>

<span data-ttu-id="d5176-159">As definições locais podem referenciar descrições geradas em outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5176-159">Local definitions can reference descriptions generated in another file.</span></span> <span data-ttu-id="d5176-160">Por exemplo, a mensagem pode ser definida no arquivo de código C gerado a partir do arquivo WSDL, mas o elemento Message pode ser definido em outro lugar no arquivo de código C gerado a partir do arquivo XSD.</span><span class="sxs-lookup"><span data-stu-id="d5176-160">For example, the message may be defined in the C code file generated from the WSDL file but the message element may be defined elsewhere in the C code file generated from the XSD file.</span></span> <span data-ttu-id="d5176-161">Nesse caso, Wsutil.exe gera referência ao elemento global do arquivo que contém a definição de mensagem, conforme demonstrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="d5176-161">In this case, Wsutil.exe generates reference to the global element from the file that contains the message definition, as demonstrated below:</span></span>

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a><span data-ttu-id="d5176-162">Descrições de elementos globais</span><span class="sxs-lookup"><span data-stu-id="d5176-162">Global element descriptions</span></span>

<span data-ttu-id="d5176-163">Para cada elemento global definido em um arquivo WSDL: Type ou XSD, há um campo correspondente chamado **ElementName** dentro do campo **globalelement** .</span><span class="sxs-lookup"><span data-stu-id="d5176-163">For each global element defined in a wsdl:type or XSD file, there is a matching field named **elementName** inside the **GlobalElement** field.</span></span> <span data-ttu-id="d5176-164">Neste exemplo, uma estrutura chamada SimpleMethod é gerada:</span><span class="sxs-lookup"><span data-stu-id="d5176-164">In this example, a structure named SimpleMethod is generated:</span></span>

``` syntax
typedef struct _SimpleServiceLocal
{
  struct  // global elements
  {
    struct // SimpleMethod
    {
    ...
    WS_ELEMENT_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    ...
  } globalElements;
}
```

<span data-ttu-id="d5176-165">Outras descrições exigidas pela descrição do elemento são geradas como parte da estrutura que a contém.</span><span class="sxs-lookup"><span data-stu-id="d5176-165">Other descriptions required by the element description are generated as part of the containing structure.</span></span> <span data-ttu-id="d5176-166">Se o elemento for um elemento de tipo simples, haverá apenas um campo de [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) .</span><span class="sxs-lookup"><span data-stu-id="d5176-166">If the element is a simple type element, there is only one [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field.</span></span> <span data-ttu-id="d5176-167">Se o tipo de elemento for uma estrutura, todos os campos relacionados e descrições de estrutura serão gerados como parte da estrutura do elemento.</span><span class="sxs-lookup"><span data-stu-id="d5176-167">If the element type is a structure, all of the related fields and structure descriptions are generated as part of the element structure.</span></span> <span data-ttu-id="d5176-168">Neste exemplo, o elemento SimpleMethod é uma estrutura que contém dois campos, **a** e **b**.</span><span class="sxs-lookup"><span data-stu-id="d5176-168">In this example, SimpleMethod element is a structure containing two fields, **a** and **b**.</span></span> <span data-ttu-id="d5176-169">Wsutil.exe gera a estrutura da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5176-169">Wsutil.exe generates the structure as follows:</span></span>

``` syntax
...
struct // SimpleMethod
{
  struct // SimpleMethod structure
  {
    WS_FIELD_DESCRIPTION a;
    WS_FIELD_DESCRIPTION b;
    WS_FIELD_DESCRIPTION * SimpleMethodFields [2];
    WS_STRUCT_DESCRIPTION structDesc;
  } SimpleMethoddescs; // SimpleMethod
  WS_ELEMENT_DESCRIPTION elementDesc;
} SimpleMethod;
...
```

<span data-ttu-id="d5176-170">Estruturas inseridas e elementos incorporados são gerados como subestruturas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d5176-170">Embedded structures and embedded elements are generated as sub-structures as needed.</span></span>

## <a name="wsdl-related-definitions"></a><span data-ttu-id="d5176-171">Definições relacionadas a WSDL</span><span class="sxs-lookup"><span data-stu-id="d5176-171">WSDL related definitions</span></span>

<span data-ttu-id="d5176-172">Wsutil.exe gera um campo sob a seção WSDL para cada um dos valores **PortType** definidos no WSDL: Service especificado.</span><span class="sxs-lookup"><span data-stu-id="d5176-172">Wsutil.exe generates a field under WSDL section for each of the **portType** values defined under the specified wsdl:service.</span></span>

``` syntax
...
struct { // WSDL
    struct { // portTypeName
        struct { // operationName
        } operationName;
    ...
    WS_OPERATION_DESCRIPTION* operations[numOperations];
    WS_CONTRACT_DESCRIPTION contractDesc;
    } portTypeName;
}
...
```

<span data-ttu-id="d5176-173">Wsutil.exe gera um campo f que contém todas as descrições necessárias para a operação, uma matriz único de ponteiros para cada uma das descrições de operação para cada método e [**uma \_ \_ Descrição de contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para o **PortType** especificado.</span><span class="sxs-lookup"><span data-stu-id="d5176-173">Wsutil.exe generates one field f that contains all the descriptions needed for the operation, a signle array of pointers to each of the operation descriptions for each method, and one [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for the specified **portType**.</span></span>

<span data-ttu-id="d5176-174">Todas as descrições necessárias pelas operações são geradas dentro do campo **operationName** sob o **PortType** especificado.</span><span class="sxs-lookup"><span data-stu-id="d5176-174">All the descriptions needed by operations are generated inside the **operationName** field under the specified **portType**.</span></span> <span data-ttu-id="d5176-175">Isso inclui o campo de [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , bem como a subestrutura para os parâmetros de entrada e saída s.</span><span class="sxs-lookup"><span data-stu-id="d5176-175">These include the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) field as well as the sub-structure for input and output parameter s.</span></span> <span data-ttu-id="d5176-176">Da mesma forma, os campos de [**\_ \_ Descrição da mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para a mensagem de entrada e a mensagem de saída opcional são incluídos junto com o; [**WS \_ Campo \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) de lista de descrição de parâmetro para todos os parâmetros de operação e o campo de [**\_ \_ Descrição da operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) para a própria operação.</span><span class="sxs-lookup"><span data-stu-id="d5176-176">Likewise, the [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) fields for the input message and the optional output message are included along with the; [**WS\_PARAMETER\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) list field for all of the operation parameters and the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) field for the operation itself.</span></span> <span data-ttu-id="d5176-177">Neste exemplo, a estrutura de código para a descrição SimpleMethod é gerada como mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="d5176-177">In this example, the code structure for the SimpleMethod description is generated as seen below:</span></span>

``` syntax
...
struct // messages
{
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_InputMessage;
  WS_MESSAGE_DESCRIPTION ISimpleService_SimpleMethod_OutputMessage;
} messages;
struct // contracts
{
  struct // DefaultBinding_ISimpleService
  {
    struct // SimpleMethod
    {
      WS_PARAMETER_DESCRIPTION params[3];
      WS_OPERATION_DESCRIPTION SimpleMethod;
    } SimpleMethod;
    WS_OPERATION_DESCRIPTION* operations[1];
    WS_CONTRACT_DESCRIPTION contractDesc;
  } DefaultBinding_ISimpleService;
} contracts;
...
```

## <a name="xml-dictionary-related-definitions"></a><span data-ttu-id="d5176-178">Definições relacionadas ao dicionário XML</span><span class="sxs-lookup"><span data-stu-id="d5176-178">XML dictionary related definitions</span></span>

<span data-ttu-id="d5176-179">Os nomes e namespaces usados em várias descrições são gerados como campos do [**tipo \_ \_ cadeia de caracteres XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span><span class="sxs-lookup"><span data-stu-id="d5176-179">Names and namespaces used in various descriptions are generated as fields of type [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string).</span></span> <span data-ttu-id="d5176-180">Todas essas cadeias de caracteres são geradas como parte de um dicionário constante por arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5176-180">All of these strings are generated as part a per-file constant dictionary.</span></span> <span data-ttu-id="d5176-181">A lista de cadeias de caracteres e o campo de [**\_ \_ dicionário XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (denominado **dictname** no exemplo abaixo) são gerados como parte do campo Dictionary da estrutura **fileNameLocal** .</span><span class="sxs-lookup"><span data-stu-id="d5176-181">The list of strings and the [**WS\_XML\_DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) field (named **dict** in the example below) are generated as part of the dictionary field of the **fileNameLocal** structure.</span></span>

``` syntax
struct { // fileNameLocal
...
  struct { // dictionary
    struct { // XML string list
      WS_XML_STRING firstFieldName;
      WS_XML_STRING firstFieldNS;
      ...
    } xmlStrings;
  WS_XML_DICTIONARY dict;
  } dictionary;
}; // fileNameLocal;
```

<span data-ttu-id="d5176-182">A matriz de [**\_ \_ cadeias de caracteres XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)é gerada como uma série de campos do tipo **cadeia de \_ \_ caracteres XML do WS**, denominada com nomes amigáveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d5176-182">The array of [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)s are generated as a series of fields of type **WS\_XML\_STRING**, named with with user-friendly names.</span></span> <span data-ttu-id="d5176-183">O stub gerado usa os nomes amigáveis em várias descrições para melhorar a legibilidade.</span><span class="sxs-lookup"><span data-stu-id="d5176-183">The generated stub uses the user-friendly names in various descriptions for better readability.</span></span>

<span data-ttu-id="d5176-184">Proxy do cliente para operações WSDL</span><span class="sxs-lookup"><span data-stu-id="d5176-184">Client proxy for WSDL operations</span></span>

<span data-ttu-id="d5176-185">Wsutil.exe gera um proxy de cliente para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="d5176-185">Wsutil.exe generates a client proxy for all of the operations.</span></span> <span data-ttu-id="d5176-186">Os aplicativos podem substituir a assinatura do método usando uma opção de linha de comando de prefixo.</span><span class="sxs-lookup"><span data-stu-id="d5176-186">Applications can overwrite the method signature using a prefix command-line option.</span></span>

``` syntax
HRESULT WINAPI bindingName_SimpleMethod(WS_SERVICE_PROXY *serviceProxy,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_CALL_PROPERTY* callProperties,
  ULONG callPropertyCount,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error )
{
  void* argList[] = {&a, &b, &c};
  return WsCall(_serviceProxy,
    (WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
    (void **)&_argList,
    callProperties,
    callPropertyCount,
    heap,
    asyncContext,
    error
  );      
}
```

<span data-ttu-id="d5176-187">O chamador da operação deve passar um parâmetro de *heap* válido.</span><span class="sxs-lookup"><span data-stu-id="d5176-187">The operation caller must pass in a valid *heap* parameter.</span></span> <span data-ttu-id="d5176-188">Os parâmetros de saída são alocados usando o valor de heap do WS \_ especificado no parâmetro *heap* .</span><span class="sxs-lookup"><span data-stu-id="d5176-188">Output parameters are allocated using the WS\_HEAP value specified in the *heap* parameter.</span></span> <span data-ttu-id="d5176-189">A função de chamada pode redefinir ou liberar o heap para liberar memória para todos os parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="d5176-189">The calling function can reset or free the heap to release memory for all of the output parameters.</span></span> <span data-ttu-id="d5176-190">Se a operação falhar, informações adicionais de erro de detalhes poderão ser recuperadas do objeto de erro opcional se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="d5176-190">If the operation fails, additional detail error information can be retrieved from the optional error object if it is available.</span></span>

<span data-ttu-id="d5176-191">Wsutil.exe gera um stub de serviço para todas as operações descritas em Binding.</span><span class="sxs-lookup"><span data-stu-id="d5176-191">Wsutil.exe generates a service stub for all of the operations described in binding.</span></span>

``` syntax
HRESULT CALLBACK ISimpleService_SimpleMethodStub(
  const WS_OPERATION_CONTEXT *context,
  void * stackStruct,
  void * callback,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR *error )
{
  SimpleMethodParamStruct *pstack = (SimpleMethodParamStruct *) stackstruct;
  SimpleMethodOperation operation = (SimpleMethodOperation)callback;
  return operation(context, pstack->a, &(pstack->b), &(pstack->c ), asyncContext, error );
}
```

<span data-ttu-id="d5176-192">A seção acima descreve o protótipo da estrutura local que contém todas as definições locais somente para o arquivo stub.</span><span class="sxs-lookup"><span data-stu-id="d5176-192">The above section describes the prototype of the local structure containing all of the definitions local to the stub file only.</span></span> <span data-ttu-id="d5176-193">As seções subsequentes descrevem as definições das descrições.</span><span class="sxs-lookup"><span data-stu-id="d5176-193">Subsequent sections describe the definitions of the descriptions.</span></span>

## <a name="wsdl-definition-generation"></a><span data-ttu-id="d5176-194">Geração de definição de WSDL</span><span class="sxs-lookup"><span data-stu-id="d5176-194">WSDL Definition Generation</span></span>

<span data-ttu-id="d5176-195">Wsutil.exe gera uma estrutura constante estática (**const estática**) chamada *<\_ nome do arquivo>* LocalDefinitions do tipo *<\_ nome do serviço>* local que contém todas as definições somente locais.</span><span class="sxs-lookup"><span data-stu-id="d5176-195">Wsutil.exe generates a constant static (**const static**) structure named *<file\_name>* LocalDefinitions of type *<service\_name>* Local that contains all the local only definitions.</span></span>

``` syntax
const static _SimpleServiceLocal example_wsdlLocalDefinitions =
{
  {  // global types
  ...
  }, // global types
  {  // global elements
  ...
  }, // global elements
  {  // messages
  ...
  }, //messages
  ...
  {  // dictionary
  ...
  }, // dictionary
},
```

<span data-ttu-id="d5176-196">Há suporte para as seguintes descrições WSDL:</span><span class="sxs-lookup"><span data-stu-id="d5176-196">The following WSDL descriptions are supported:</span></span>

-   <span data-ttu-id="d5176-197">WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="d5176-197">wsdl:service</span></span>
-   <span data-ttu-id="d5176-198">WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="d5176-198">wsdl:binding</span></span>
-   <span data-ttu-id="d5176-199">WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="d5176-199">wsdl:portType</span></span>
-   <span data-ttu-id="d5176-200">WSDL: operação</span><span class="sxs-lookup"><span data-stu-id="d5176-200">wsdl:operation</span></span>
-   <span data-ttu-id="d5176-201">WSDL: mensagem</span><span class="sxs-lookup"><span data-stu-id="d5176-201">wsdl:message</span></span>

## <a name="processing-wsdloperation-and-wsdlmessage"></a><span data-ttu-id="d5176-202">Processando WSDL: Operation e WSDL: Message</span><span class="sxs-lookup"><span data-stu-id="d5176-202">Processing wsdl:operation and wsdl:message</span></span>

<span data-ttu-id="d5176-203">Cada operação especificada no documento WSDL é mapeada para uma operação de serviço por [Wsutil.exe](web-service-compiler-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d5176-203">Each operation specified in the WSDL document is mapped to a service operation by [Wsutil.exe](web-service-compiler-tool.md).</span></span> <span data-ttu-id="d5176-204">A ferramenta gera definições separadas das operações de serviço para o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="d5176-204">The tool generates separate definitions of the service operations for both the server and the client.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   <wsdl:input wsaw:Action="http://Example.org/ISimpleService/SimpleMethod" 
   message="tns:ISimpleService_SimpleMethod_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ISimpleService/SimpleMethodResponse" 
   message="tns:ISimpleService_SimpleMethod_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="d5176-205">O layout dos elementos de dados da mensagem andoutput de entrada é avaliado pela ferramenta para gerar os metadados de serialização para a infraestrutura, juntamente com a assinatura real da operação de serviço resultante à qual as mensagens de entrada e saída estão associadas.</span><span class="sxs-lookup"><span data-stu-id="d5176-205">The layout of the input andoutput message data elements is evaluated by the tool to generate the serialization metadata for the infrastructure along with the actual signature of the resulting service operation to which the input and output messages are associated.</span></span>

<span data-ttu-id="d5176-206">Os metadados de cada operação dentro de um **PortType** específico têm entrada e, opcionalmente, uma mensagem de saída, cada uma dessas mensagens é mapeada para uma [**\_ \_ Descrição de mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span><span class="sxs-lookup"><span data-stu-id="d5176-206">The metadata for each operation within a specific **portType** has input and optionally an output message, each of these messages is mapped to a [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description).</span></span> <span data-ttu-id="d5176-207">Neste exemplo, a entrada e a mensagem de saída na operação em portType mapeado para inputMessageDescription e, opcionalmente, o outputMessageDescription na [**Descrição da \_ operação \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5176-207">In this example, the input and the output message on the operation in the portType mapped to inputMessageDescription and optionally the outputMessageDescription on the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) respectively.</span></span>

<span data-ttu-id="d5176-208">Para cada mensagem WSDL, a ferramenta gera a [**\_ \_ Descrição da mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) que faz referência à definição da [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , conforme demonstrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="d5176-208">For each WSDL message the tool generates [**WS\_MESSAGE\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) that references the [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) definition, as demonstrated below:</span></span>

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="d5176-209">A descrição da mensagem refere-se à descrição do elemento de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5176-209">The message description refers to the input element description.</span></span> <span data-ttu-id="d5176-210">Como o elemento é definido globalmente, a descrição da mensagem faz referência à definição global em vez do elemento estático local.</span><span class="sxs-lookup"><span data-stu-id="d5176-210">Because the element is globally defined, the message description references the global definition instead of the local static element.</span></span> <span data-ttu-id="d5176-211">Da mesma forma, se o elemento for definido em outro arquivo, Wsutil.exe gerará uma referência à estrutura definida globalmente nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5176-211">Similarly, if the element is defined in another file, Wsutil.exe generates a reference to the globally-defined structure in that file.</span></span> <span data-ttu-id="d5176-212">Por exemplo, se SimpleMethodResponse for definido em outro arquivo. xsd de exemplo, Wsutil.exe gerará o seguinte em vez disso:</span><span class="sxs-lookup"><span data-stu-id="d5176-212">For example, if SimpleMethodResponse is defined in another example.xsd file, Wsutil.exe generates the following instead:</span></span>

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

<span data-ttu-id="d5176-213">Cada descrição da mensagem contém a ação e a descrição do elemento específico (um campo do tipo [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) para todos os elementos de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-213">Each message description contains the action and the specific element description (a field of type [**WS\_ELEMENT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) for all the message data elements.</span></span> <span data-ttu-id="d5176-214">No caso de uma mensagem em estilo RPC ou uma mensagem com várias partes, um elemento wrapper é criado para encapsular as informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="d5176-214">In the case of an RPC-style message or a message with multiple parts, a wrapper element is created to encapsulate the additional information.</span></span>

## <a name="rpc-style-support"></a><span data-ttu-id="d5176-215">Suporte ao estilo RPC</span><span class="sxs-lookup"><span data-stu-id="d5176-215">RPC style support</span></span>

<span data-ttu-id="d5176-216">Wsutil.exe dá suporte ao estilo de documento, bem como a operações de estilo RPC de acordo com a extensão de associação WSDL 1,1 para a especificação SOAP 1,2.</span><span class="sxs-lookup"><span data-stu-id="d5176-216">Wsutil.exe supports document-style as well as RPC-style operations according to the WSDL 1.1 Binding Extension for SOAP 1.2 specification.</span></span> <span data-ttu-id="d5176-217">As operações de estilo RPC e literal são marcadas como \_ operação WS RPC \_ literal \_ .</span><span class="sxs-lookup"><span data-stu-id="d5176-217">RPC- and literal-style operations are marked as WS\_RPC\_LITERAL\_OPERATION.</span></span> <span data-ttu-id="d5176-218">O modelo de serviço ignora o nome do elemento wrapper de corpo de resposta em operações RPC/literal.</span><span class="sxs-lookup"><span data-stu-id="d5176-218">The service model ignores the name for the response body wrapper element in RPC/literal operations.</span></span>

<span data-ttu-id="d5176-219">Wsutil.exe não oferece suporte nativo a operações de estilo de codificação.</span><span class="sxs-lookup"><span data-stu-id="d5176-219">Wsutil.exe does not natively support encoding-style operations.</span></span> <span data-ttu-id="d5176-220">O \_ parâmetro de buffer XML do WS \_ é gerado para mensagens de codificação e os desenvolvedores devem preencher o buffer opaco diretamente.</span><span class="sxs-lookup"><span data-stu-id="d5176-220">The WS\_XML\_BUFFER parameter is generated for encoding messages, and developers must populate the opaque buffer directly.</span></span>

## <a name="multiple-message-parts-support"></a><span data-ttu-id="d5176-221">Suporte a várias partes de mensagens</span><span class="sxs-lookup"><span data-stu-id="d5176-221">Multiple message parts support</span></span>

<span data-ttu-id="d5176-222">O Wsutil.exe dá suporte a várias partes de mensagem em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-222">Wsutil.exe supports multiple message parts in one message.</span></span> <span data-ttu-id="d5176-223">Uma mensagem de várias partes pode ser especificada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5176-223">A multi-part message can be specified as follows:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_MutipleParts_InputMessage">
  <wsdl:part name="part1" element="tns:SimpleElement1" />
  <wsdl:part name="part2" element="tns:SimpleElement2" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="d5176-224">Wsutil.exe gera um campo de [**\_ \_ tipo struct do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para o elemento Message se a mensagem contiver várias partes.</span><span class="sxs-lookup"><span data-stu-id="d5176-224">Wsutil.exe generates a [**WS\_STRUCT\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) field for the message element if the message contains multiple parts.</span></span> <span data-ttu-id="d5176-225">Se a mensagem for representada usando o estilo do documento, Wsutil.exe gerará um elemento wrapper com o tipo struct.</span><span class="sxs-lookup"><span data-stu-id="d5176-225">If the message is represented using the document style, Wsutil.exe generates a wrapper element with struct type.</span></span> <span data-ttu-id="d5176-226">O elemento wrapper não tem um nome ou um namespace específico, e a estrutura do wrapper contém todos os elementos de todas as partes como campos.</span><span class="sxs-lookup"><span data-stu-id="d5176-226">The wrapper element does not have a name or a specific namespace, and the wrapper structure contains all of the elements in all of the parts as fields.</span></span> <span data-ttu-id="d5176-227">O elemento wrapper é somente para uso interno e não será serializado no corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-227">The wrapper element is for internal use only and it will not be serialized in the message body.</span></span>

<span data-ttu-id="d5176-228">Se a mensagem estiver usando a representação de estilo de RPC ou literal, Wsutil.exe criará um elemento wrapper com o nome da operação como o nome do elemento e o namespace especificado como namespace de serviço, de acordo com a especificação de extensão SOAP WSDL.</span><span class="sxs-lookup"><span data-stu-id="d5176-228">If the message is using RPC or literal style representation , Wsutil.exe creates a wrapper element with the operation name as the element name and the specified namespace as service namespace according to WSDL SOAP extension specification.</span></span> <span data-ttu-id="d5176-229">A estrutura do elemento contém uma matriz de campos que representa os tipos especificados nas partes da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-229">The structure of the element contains an array of fields representing the types specified in the message parts.</span></span> <span data-ttu-id="d5176-230">O elemento wrapper é mapeado para o elemento top real no corpo da mensagem, conforme indicado na especificação SOAP.</span><span class="sxs-lookup"><span data-stu-id="d5176-230">The wrapper element is mapped to the actual top element in message body as indicated in the SOAP specification.</span></span>

<span data-ttu-id="d5176-231">No lado do servidor, cada operação resulta em um typedef da operação de serviço do servidor resultante.</span><span class="sxs-lookup"><span data-stu-id="d5176-231">On the server side, each operation results in a typedef of the resulting server service operation.</span></span> <span data-ttu-id="d5176-232">Esse typedef é usado para fazer referência à operação na tabela de funções, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5176-232">This typedef is used to refer to the operation in the function table as described previously.</span></span> <span data-ttu-id="d5176-233">Cada operação também resulta na geração de uma função de stub que nfrastructure chamadas em nome do delegado para o método real.</span><span class="sxs-lookup"><span data-stu-id="d5176-233">Every operation also results in the generation of a stub function which nfrastructure calls on behalf of the delegate to the actual method.</span></span>

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT* context,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error
  );
```

<span data-ttu-id="d5176-234">Para a operação SimpleMethod, o typedef SimpleMethodOperation é definido acima.</span><span class="sxs-lookup"><span data-stu-id="d5176-234">For the SimpleMethod operation, the SimpleMethodOperation typedef is defined above.</span></span> <span data-ttu-id="d5176-235">Observe que o método gerado tem um argumento expandido listwith a parte da mensagem para a mensagem de entrada e saída para a operação SimpleMethod como parâmetros nomeados.</span><span class="sxs-lookup"><span data-stu-id="d5176-235">Note that the generated method has an expanded argument listwith the message part for the input and output message for SimpleMethod operation as named parameters.</span></span>

<span data-ttu-id="d5176-236">No lado do cliente, cada operação é mapeada para uma operação de serviço de proxy.</span><span class="sxs-lookup"><span data-stu-id="d5176-236">On the client side each operation is mapped to a proxy service operation.</span></span>

``` syntax
HRESULT WINAPI SimpleMethod (
  WS_SERVICE_PROXY* serviceProxy,
  ws_heap *heap,
  unsigned int  a,
  unsigned int * b,
  unsigned int * c,
  const WS_ASYNC_CONTEXT* asyncContext,
  WS_ERROR* error);
```

## <a name="processing-wsdlbinding"></a><span data-ttu-id="d5176-237">Processando WSDL: Binding</span><span class="sxs-lookup"><span data-stu-id="d5176-237">Processing wsdl:binding</span></span>

<span data-ttu-id="d5176-238">O modelo de serviço WWSAPI dá suporte à extensão de associação SOAP.</span><span class="sxs-lookup"><span data-stu-id="d5176-238">The WWSAPI service model supports theSOAP binding extension.</span></span> <span data-ttu-id="d5176-239">Para cada associação, há um **PortType** associado.</span><span class="sxs-lookup"><span data-stu-id="d5176-239">For each binding there is an associated **portType**.</span></span>

<span data-ttu-id="d5176-240">O transporte especificado na extensão de ligação SOAP é apenas para consultoria.</span><span class="sxs-lookup"><span data-stu-id="d5176-240">The transport specified in soap binding extension is advisory only.</span></span> <span data-ttu-id="d5176-241">O aplicativo precisa fornecer informações de transporte ao criar um canal.</span><span class="sxs-lookup"><span data-stu-id="d5176-241">Application needs to provide transport information when creating a channel.</span></span> <span data-ttu-id="d5176-242">Atualmente, damos suporte à \_ Associação http WS \_ e \_ associações de associação TCP WS \_ .</span><span class="sxs-lookup"><span data-stu-id="d5176-242">Currently we support the WS\_HTTP\_BINDING and WS\_TCP\_BINDING bindings.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:binding name="DefaultBinding_ISimpleService" type="tns:ISimpleService">
  <soap:binding transport="http://schemas.xmlsoap.org/soap/http" />
  <wsdl:operation name="SimpleMethod">
   <soap:operation soapAction="http://Example.org/ISimpleService/SimpleMethod" 
   style="document" />
   <wsdl:input>
    <soap:body use="literal" />
   </wsdl:input>
   <wsdl:output>
    <soap:body use="literal" />
   </wsdl:output>
  </wsdl:operation>
 </wsdl:binding>
</wsdl:definitions>
```

<span data-ttu-id="d5176-243">Em nosso documento WSDL de exemplo, temos apenas um **PortType** para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="d5176-243">In our example WSDL document we only have one **portType** for ISimpleService.</span></span> <span data-ttu-id="d5176-244">A associação SOAP fornecida indica o transporte HTTP, que é especificado como \_ Associação http WS \_ .</span><span class="sxs-lookup"><span data-stu-id="d5176-244">The provided SOAP binding indicates the HTTP transport, which is specified as WS\_HTTP\_BINDING.</span></span> <span data-ttu-id="d5176-245">Observe que essa estrutura não tem decoração estática, pois essa estrutura precisa estar disponível para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5176-245">Notice that this structure does not have static decoration as this structure needs to be available to the application.</span></span>

<span data-ttu-id="d5176-246">Processando WSDL: portType</span><span class="sxs-lookup"><span data-stu-id="d5176-246">Processing wsdl:portType</span></span>

<span data-ttu-id="d5176-247">Cada **PortType** no WSDL é constituído de uma ou mais operações.</span><span class="sxs-lookup"><span data-stu-id="d5176-247">Each **portType** in WSDL is made up of one or more operations.</span></span> <span data-ttu-id="d5176-248">A operação deve ser consistente com a extensão de ligação SOAP indicada em WSDL: Binding.</span><span class="sxs-lookup"><span data-stu-id="d5176-248">The operation should be consistent with the SOAP binding extension indicated in wsdl:binding.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ISimpleService">
  <wsdl:operation name="SimpleMethod">
   ...
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="d5176-249">Neste exemplo, o **PortType** ISimpleService contém apenas a operação SimpleMethod.</span><span class="sxs-lookup"><span data-stu-id="d5176-249">In this example, the ISimpleService **portType** only contains the SimpleMethod operation.</span></span> <span data-ttu-id="d5176-250">Isso é consistente com a seção de associação em que há apenas uma operação WSDL que é mapeada para uma ação SOAP.</span><span class="sxs-lookup"><span data-stu-id="d5176-250">This is consistent with the binding section where there is only one WSDL operation that maps to a SOAP action.</span></span>

<span data-ttu-id="d5176-251">Como o **PortType** ISimpleService tem apenas uma operação--SimpleMethod--a tabela de funções correspondente contém apenas SimpleMethod como uma operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-251">Since the ISimpleService **portType** only has one operation -- SimpleMethod -- the corresponding function table only contains SimpleMethod as a service operation.</span></span>

<span data-ttu-id="d5176-252">Em termos de metadados, cada **PortType** é mapeado por Wsutil.exe para [**uma \_ \_ Descrição de contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span><span class="sxs-lookup"><span data-stu-id="d5176-252">In terms of metadata each **portType** is mapped by Wsutil.exe to a [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description).</span></span> <span data-ttu-id="d5176-253">Cada operação dentro de um **PortType** é mapeada para [**uma \_ \_ Descrição de operação do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span><span class="sxs-lookup"><span data-stu-id="d5176-253">Each operation within a **portType** is mapped to a [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).</span></span>

<span data-ttu-id="d5176-254">Neste exemplo, **PortType** a ferramenta gera a [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="d5176-254">In this example, **portType** the tool generates [**WS\_CONTRACT\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) for ISimpleService.</span></span> <span data-ttu-id="d5176-255">Esta descrição do contrato contém o número específico de operações disponíveis no **PortType** ISimpleService junto com uma matriz de [**\_ \_ Descrição da operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) que representa as operações individuais definidas em PortType para ISimpleService.</span><span class="sxs-lookup"><span data-stu-id="d5176-255">This contract description contains the specific number of operations available on the ISimpleService **portType** along with an array of [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) representing the individual operations defined on the portType for ISimpleService.</span></span> <span data-ttu-id="d5176-256">Como há apenas uma operação em portType ISimpleService para ISimpleService, também há apenas uma definição de **\_ \_ Descrição de operação do WS** .</span><span class="sxs-lookup"><span data-stu-id="d5176-256">Since there is only one operation on ISimpleService portType for ISimpleService, there is also only one **WS\_OPERATION\_DESCRIPTION** definition.</span></span>

``` syntax
...  part of LocalDefinitions structure
{    // array of operations for DefaultBinding_ISimpleService
(WS_OPERATION_DESCRIPTION*)&example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.SimpleMethod,
},    // array of operations for DefaultBinding_ISimpleService
{    // contract description for DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},  // end of contract description for DefaultBinding_ISimpleService
},    // DefaultBinding_ISimpleService       ...
```

## <a name="processing-wsdlservice"></a><span data-ttu-id="d5176-257">Processando WSDL: Service</span><span class="sxs-lookup"><span data-stu-id="d5176-257">Processing wsdl:service</span></span>

<span data-ttu-id="d5176-258">O WsUtil.exe usa os serviços para encontrar Associação/PortType e gera a estrutura de contrato que descreve tipos, mensagens, definições PortType e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d5176-258">WsUtil.exe uses the services to find binding/porttypes, and generates contract structure that describes types, message, porttype definitions, and so on.</span></span> <span data-ttu-id="d5176-259">As descrições de contrato são acessíveis externamente e são geradas como parte da estrutura de definição global especificada por meio do cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="d5176-259">Contract descriptions are externally accessible, and they are generated as part of the global definition structure specified through generated header.</span></span>

<span data-ttu-id="d5176-260">O WsUtil.exe dá suporte a extensões EndpointReference definidas em WSDL: Port.</span><span class="sxs-lookup"><span data-stu-id="d5176-260">WsUtil.exe supports EndpointReference extensions defined in wsdl:port.</span></span> <span data-ttu-id="d5176-261">A referência de ponto de extremidade é definida no WS-ADDRESSing como uma maneira de descrever informações de [ponto de extremidade](endpoint-address.md) de um serviço.</span><span class="sxs-lookup"><span data-stu-id="d5176-261">Endpoint reference is defined in WS-ADDRESSING as a way to describe [endpoint](endpoint-address.md) information of a service.</span></span> <span data-ttu-id="d5176-262">O texto da extensão de referência do ponto de extremidade de entrada salvo como [**\_ cadeia de \_ caracteres XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), junto com a descrição correspondente do [**\_ \_ endereço \_ de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) , é gerado na seção endpointReferences na estrutura global.</span><span class="sxs-lookup"><span data-stu-id="d5176-262">The input endpoint reference extension text saved as [**WS\_XML\_STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), together with matching [**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) are generated in endpointReferences section in the global structure.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:service name="SimpleService">
  <wsdl:port name="ISimpleService" binding="tns:DefaultBinding_ISimpleService">
   <soap:address location="http://Example.org/ISimpleService" />
   <wsa:EndpointReference>
    <wsa:Address>http://example.org/wcfmetadata/WSHttpNon</wsa:Address>
   </wsa:EndpointReference> 
  </wsdl:port>
 </wsdl:service>
</wsdl:definitions>
```

``` syntax
  const _example_wsdl example_wsdl =
  {
  ... // global element description
  {// messages
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
},    // message description for ISimpleService_SimpleMethod_InputMessage
{    // message description for ISimpleService_SimpleMethod_OutputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_OutputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodResponse,
},    // message description for ISimpleService_SimpleMethod_OutputMessage
}, // messages
{// contracts
{   // DefaultBinding_ISimpleService
1,
(WS_OPERATION_DESCRIPTION**)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.operations,
WS_HTTP_CHANNEL_BINDING,
},    // end of DefaultBinding_ISimpleService
    }, // contracts
    {
        {
            {   // endpointAddressDescription
                WS_ADDRESSING_VERSION_0_9,
            },                    
            (WS_XML_STRING*)&xml_string_generated_in_stub // endpointReferenceString
        }, //DefaultBinding_ISimpleService
    }, // endpointReferences
}
```

<span data-ttu-id="d5176-263">Para criar [**um \_ \_ endereço de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) usando os metadados gerados pelo WsUtil:</span><span class="sxs-lookup"><span data-stu-id="d5176-263">To Create [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) using the WsUtil generated metadata:</span></span>

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

<span data-ttu-id="d5176-264">As cadeias de caracteres constantes no proxy do cliente ou no stub do serviço são geradas como campos do tipo \_ cadeia de caracteres XML do WS \_ , e há um dicionário constante para todas as cadeias de caracteres no arquivo de proxy ou de stub.</span><span class="sxs-lookup"><span data-stu-id="d5176-264">Constant strings in the client proxy or service stub are generated as fields of type WS\_XML\_STRING, and there is a constant dictionary for all the strings in the proxy or stub file.</span></span> <span data-ttu-id="d5176-265">Cada cadeia de caracteres no dicionário é gerada como um campo na parte de dicionário da estrutura local para melhorar a legibilidade.</span><span class="sxs-lookup"><span data-stu-id="d5176-265">Each string in the dictionary is generated as a field in the dictionary part of the local structure for better readability.</span></span>

``` syntax
... // dictionary part of LocalDefinitions structure
{    // xmlStrings
  { // xmlStrings
    WS_XML_STRING_DICTIONARY_VALUE("a",&example_wsdlLocalDefinitions.dictionary.dict, 0), 
    WS_XML_STRING_DICTIONARY_VALUE("http://Sapphire.org",&example_wsdlLocalDefinitions.dictionary.dict, 1), 
    WS_XML_STRING_DICTIONARY_VALUE("b",&example_wsdlLocalDefinitions.dictionary.dict, 2), 
    WS_XML_STRING_DICTIONARY_VALUE("SimpleMethod",&example_wsdlLocalDefinitions.dictionary.dict, 3),
    ...
  },  // end of xmlStrings
  {   // SimpleServicedictionary
    // 45026280-d5dc-4570-8195-4d66d13bfa34
    { 0x45026280, 0xd5dc, 0x4570, { 0x81, 0x95, 0x4d,0x66, 0xd1, 0x3b, 0xfa, 0x34 } },
    (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings,
    stringCount,
    TRUE,
  },
}
...
```

## <a name="processing-wsdltype"></a><span data-ttu-id="d5176-266">Processando WSDL: Type</span><span class="sxs-lookup"><span data-stu-id="d5176-266">Processing wsdl:type</span></span>

<span data-ttu-id="d5176-267">Wsutil.exe dá suporte apenas a documentos XSD (esquema XML) em especificação WSDL: Type.</span><span class="sxs-lookup"><span data-stu-id="d5176-267">Wsutil.exe only supports XML schema (XSD) documents in wsdl:type specification.</span></span> <span data-ttu-id="d5176-268">Um caso especial é quando uma porta de mensagem Especifica uma definição de elemento global.</span><span class="sxs-lookup"><span data-stu-id="d5176-268">One special case is when a message port specifies a global element definition.</span></span> <span data-ttu-id="d5176-269">Consulte a seção a seguir para obter mais detalhes sobre a heurística usada nesses casos.</span><span class="sxs-lookup"><span data-stu-id="d5176-269">See the following section for more details of the heuristics used in these cases.</span></span>

## <a name="parameter-processing-heuristics"></a><span data-ttu-id="d5176-270">Heurística de processamento de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5176-270">Parameter Processing Heuristics</span></span>

<span data-ttu-id="d5176-271">No modelo de serviço, as mensagens WSDL são mapeadas para parâmetros específicos em um método.</span><span class="sxs-lookup"><span data-stu-id="d5176-271">In the service model, WSDL messages are mapped to specific parameters in a method.</span></span> <span data-ttu-id="d5176-272">Wsutil.exe tem dois estilos de geração de parâmetro: no primeiro estilo, a operação tem um parâmetro para a mensagem de entrada e um parâmetro para a mensagem de saída (se necessário); no segundo estilo, Wsutil.exe usa uma heurística para mapear e expandir os campos nas estruturas para mensagens de entrada e mensagens de saída para parâmetros diferentes na operação.</span><span class="sxs-lookup"><span data-stu-id="d5176-272">Wsutil.exe has two styles of parameter generation: in first style, the operation has one parameter for input message, and one parameter for output message (if necessary); in the second style, Wsutil.exe uses a heuristic to map and expand fields in the structures for both input messages and output messages to different parameters in the operation.</span></span> <span data-ttu-id="d5176-273">As mensagens de entrada e saída precisam ter elementos de mensagem de tipo de estrutura para gerar essa segunda abordagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-273">Both input and output messages need to have structure type message elements to generate this second approach.</span></span>

<span data-ttu-id="d5176-274">Wsutil.exe usa as seguintes regras ao gerar parâmetros de operação das mensagens de entrada e saída:</span><span class="sxs-lookup"><span data-stu-id="d5176-274">Wsutil.exe uses the following rules when generating operation parameters from the input and output messages:</span></span>

-   <span data-ttu-id="d5176-275">Para mensagens de entrada e saída com várias partes de mensagem, cada parte de mensagem é um parâmetro separado na operação, com o nome da parte da mensagem como nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-275">For input and output messages with multiple message parts, each message part is a separate parameter in the operation, with the message part name as parameter name.</span></span>
-   <span data-ttu-id="d5176-276">Para a mensagem de estilo RPC com uma parte de mensagem, a parte da mensagem é um parâmetro na operação, com o nome da parte da mensagem como nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-276">For RPC style message with one message part, the message part is a parameter in the operation, with message part name as parameter name.</span></span>
-   <span data-ttu-id="d5176-277">Para mensagens de entrada e saída no estilo de documento com uma parte de mensagem:</span><span class="sxs-lookup"><span data-stu-id="d5176-277">For document-style input and output messages with one message part:</span></span>
    -   <span data-ttu-id="d5176-278">Se o nome de uma parte de mensagem for "Parameters" e o tipo de elemento for uma estrutura, cada campo na estrutura será tratado como um parâmetro separado com o nome do campo sendo o nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-278">If the name of a message part is "parameters" and the element type is a structure, each field in the structure is treated as a separate parameter with the field name being the parameter name.</span></span>
    -   <span data-ttu-id="d5176-279">Se o nome da parte da mensagem não for "Parameters", a mensagem será um parâmetro na operação com o nome da mensagem usado como o nome do parâmetro correspondente.</span><span class="sxs-lookup"><span data-stu-id="d5176-279">If the message part name is not "parameters", the message is a parameter in the operation with the message name used as the corresponding parameter name.</span></span>
-   <span data-ttu-id="d5176-280">Para a mensagem de entrada e saída do estilo do documento com o elemento anulável, a mensagem é mapeada para um parâmetro, com o nome da parte da mensagem como nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-280">For document style input and output message with nillable element, the message is mapped to one parameter, with message part name as parameter name.</span></span> <span data-ttu-id="d5176-281">Um nível adicional de indireção é adicionado para indicar que o ponteiro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d5176-281">One additional level of indirection is added to indicate the pointer can be **NULL**.</span></span>
-   <span data-ttu-id="d5176-282">Se um campo aparecer apenas no elemento de mensagem de entrada, o campo será tratado como \[ um \] parâmetro in.</span><span class="sxs-lookup"><span data-stu-id="d5176-282">If a field appears in the input message element only, the field is treated as an \[in\] parameter.</span></span>
-   <span data-ttu-id="d5176-283">Se um campo aparecer somente no elemento de mensagem de saída, o campo será tratado como \[ um \] parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="d5176-283">If a field appears in the output message element only, the field is treated as an \[out\] parameter.</span></span>
-   <span data-ttu-id="d5176-284">Se houver um campo com o mesmo nome e o mesmo tipo que aparece na mensagem de entrada e na mensagem de saída, o campo será tratado como um \[ parâmetro in e out \] .</span><span class="sxs-lookup"><span data-stu-id="d5176-284">If there is a field with the same name and same type that appears in both the input message and the output message, the field is treated as an \[in,out\] parameter.</span></span>

<span data-ttu-id="d5176-285">As ferramentas a seguir são usadas para determinar a direção dos parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d5176-285">Following tools are used to determine the direction of parameters:</span></span>

-   <span data-ttu-id="d5176-286">Se um campo aparecer apenas no elemento de mensagem de entrada, o campo será tratado como somente no parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-286">If a field appears in input message element only, the field is treated as in only parameter.</span></span>
-   <span data-ttu-id="d5176-287">Se um campo aparecer apenas no elemento de mensagem de saída, o campo será tratado como somente parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5176-287">If a field appears in output message element only, the field is treated as out only parameter.</span></span>
-   <span data-ttu-id="d5176-288">Se houver um campo com o mesmo nome e o mesmo tipo que aparece na mensagem de entrada e na mensagem de saída, o campo será tratado como um parâmetro in e out.</span><span class="sxs-lookup"><span data-stu-id="d5176-288">If there is a field with the same name and same type that appears in both input message and output message, the field is treated as an in,out parameter.</span></span>

<span data-ttu-id="d5176-289">Wsutil.exe só dá suporte a elementos sequenciados.</span><span class="sxs-lookup"><span data-stu-id="d5176-289">Wsutil.exe only supports sequenced elements.</span></span> <span data-ttu-id="d5176-290">Ele rejeita a ordenação inválida com relação aos \[ parâmetros de saída \] se Wsutil.exe não pode combinar os parâmetros in e out em uma única lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d5176-290">It rejects invalid ordering with regard to \[in,out\] parameters if Wsutil.exe cannot combine the in parameters and out parameters into a single parameter list.</span></span> <span data-ttu-id="d5176-291">Os sufixos podem ser adicionados aos nomes de parâmetro para evitar a colisão de nomes.</span><span class="sxs-lookup"><span data-stu-id="d5176-291">Suffixes might be added to parameter names to avoid name collision.</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:message name="ISimpleService_SimpleMethod_InputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethod" />
 </wsdl:message>
 <wsdl:message name="ISimpleService_SimpleMethod_OutputMessage">
  <wsdl:part name="parameters" element="tns:SimpleMethodResponse" />
 </wsdl:message>
</wsdl:definitions>
```

<span data-ttu-id="d5176-292">Wsutil.exe considera os campos em TNS: SimpleMethod e TNS: SimpleMethodResponse ato são parâmetros, como visto nas definições de parâmetro abaixo:</span><span class="sxs-lookup"><span data-stu-id="d5176-292">Wsutil.exe considers fields in tns:SimpleMethod and tns:SimpleMethodResponse ato be parameters, as seen in the parameter definitions below:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
  targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
   <xs:import namespace="http://Example.org" />
   <xs:element name="SimpleMethod">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="a" type="xs:unsignedInt" />
      <xs:element name="b" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
   <xs:element name="SimpleMethodResponse">
    <xs:complexType>
     <xs:sequence>
      <xs:element name="b" type="xs:unsignedInt" />
      <xs:element name="c" type="xs:unsignedInt" />
     </xs:sequence>
    </xs:complexType>
   </xs:element>
  </xs:schema>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="d5176-293">Wsutil.exe expande a lista de parâmetros dos campos na lista acima e gera a estrutura **ParamStruct** no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5176-293">Wsutil.exe expands the parameter list from the fields in the list above, and generates the **ParamStruct** structure in the following code example.</span></span> <span data-ttu-id="d5176-294">O tempo de execução do modelo de serviço pode usar essa estrutura para passar argumentos para os stubs do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="d5176-294">The service model run-time can use this structure to pass arguments to the client and server stubs.</span></span>

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

<span data-ttu-id="d5176-295">Essa estrutura é usada apenas para descrever o quadro de pilha no cliente e no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="d5176-295">This structure is only used to describe the stack frame on the client and server side.</span></span> <span data-ttu-id="d5176-296">Não há nenhuma alteração na descrição da mensagem ou nas descrições de elemento referenciadas pela descrição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5176-296">There is no change to the message description, or to the element descriptions referenced by the message description.</span></span>

``` syntax
  // following are local definitions for the complex type
  { // field description for a
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, a),
  0,
  0,
  },    // end of field description for a
  { // field description for b
  WS_ELEMENT_FIELD_MAPPING,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.bLocalName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_INT32_TYPE,
  0,
  WsOffsetOf(_SimpleMethod, b),
  0,
  0,
  },    // end of field description for b
  {    // fields description for _SimpleMethod
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.a,
  (WS_FIELD_DESCRIPTION *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.b,
  },
  {  // structure definition
  sizeof(_SimpleMethod),
  __alignof(_SimpleMethod),
  (WS_FIELD_DESCRIPTION**)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields,
  WsCountOf(example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs._SimpleMethodFields),
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  0,
  },   // struct description for _SimpleMethod
  // following are global definitions for the out parameter
  ...
  {  // element description
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings._SimpleMethodTypeName,
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.aNamespace,
  WS_STRUCT_TYPE,
  (void *)&example_wsdlLocalDefinitions.globalElements.SimpleMethod._SimpleMethoddescs.structDesc,
  },
  {    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.ISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethod,
  },    // message description for ISimpleService_SimpleMethod_InputMessage
```

<span data-ttu-id="d5176-297">Como regra geral, um nível de indireção é adicionado para todos os \[ \] parâmetros out e \[ in, out \] .</span><span class="sxs-lookup"><span data-stu-id="d5176-297">As a general rule, one level of indirection is added for all the \[out\] and \[in,out\] parameters.</span></span>

## <a name="parameterless-operation"></a><span data-ttu-id="d5176-298">Operação sem parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5176-298">Parameterless operation</span></span>

<span data-ttu-id="d5176-299">Para operações de documento e literal, Wsutil.exe trata a operação como tendo um parâmetro de entrada e um parâmetro de saída se:</span><span class="sxs-lookup"><span data-stu-id="d5176-299">For document and literal operations, Wsutil.exe treats the operation as having one input parameter and one output parameter if:</span></span>

-   <span data-ttu-id="d5176-300">A mensagem de entrada ou saída tem mais de uma parte.</span><span class="sxs-lookup"><span data-stu-id="d5176-300">The input or output message has more than one part.</span></span>
-   <span data-ttu-id="d5176-301">Há apenas uma parte de mensagem e o nome da parte da mensagem não é "parâmetros".</span><span class="sxs-lookup"><span data-stu-id="d5176-301">There is only one message part and the message part name is not "parameters".</span></span>

<span data-ttu-id="d5176-302">..</span><span class="sxs-lookup"><span data-stu-id="d5176-302">..</span></span> <span data-ttu-id="d5176-303">No exemplo acima, supondo que as partes da mensagem sejam chamadas *parame*"e *paramout*, a assinatura do método se torna o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="d5176-303">In the example above, assuming the message parts are named *ParamIn*" and *ParamOut*, the method signature becomes the following code:</span></span>

``` syntax
typedef struct SimpleMethod{
unsigned int a;
unsigned int b;
};

typedef struct SimpleMethodResponse {
unsigned int b;
unsigned int c;
};

typedef  struct ISimpleService_SimpleMethodParamStruct
{
SimpleMethod  * SimpleMethod;
SimpleMethodResponse  * SimpleMethodResponse;
} ISimpleService_SimpleMethodParamStruct;
```

<span data-ttu-id="d5176-304">Wsutil.exe gera uma assinatura de versão para a descrição da operação de modo que o WsCall e o mecanismo de modelo de serviço do lado do servidor possam verificar se a descrição gerada é aplicável para a plataforma atual.</span><span class="sxs-lookup"><span data-stu-id="d5176-304">Wsutil.exe generates a version signature for the operation description such that the WsCall and server-side service model engine can check if the generated description is applicable for the current platform.</span></span>

<span data-ttu-id="d5176-305">Essas informações de versão são geradas como parte da estrutura de [**\_ \_ Descrição da operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) .</span><span class="sxs-lookup"><span data-stu-id="d5176-305">This version info is generated as part of the [**WS\_OPERATION\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) structure.</span></span> <span data-ttu-id="d5176-306">O número de versão pode ser tratado como um seletor de União Union para tornar a estrutura extensível.</span><span class="sxs-lookup"><span data-stu-id="d5176-306">The version number can be treated as a union arm selector to make the structure extensible.</span></span> <span data-ttu-id="d5176-307">Atualmente, **VersionId** é definido como to1 sem nenhum campo subsequente.</span><span class="sxs-lookup"><span data-stu-id="d5176-307">Currently, the **versionID** is set to1 with no subsequent fields.</span></span> <span data-ttu-id="d5176-308">O futuro versiosn pode incrementar o número de versão e incluir mais campos, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d5176-308">Future versiosn may increment the version number and include more fields as needed.</span></span> <span data-ttu-id="d5176-309">Por exemplo, Wsutil.exe gera atualmente o seguinte código com base na ID de versão:</span><span class="sxs-lookup"><span data-stu-id="d5176-309">For example, Wsutil.exe currently generates the following code based on the version ID:</span></span>

``` syntax
{ // SimpleMethod
{ // parameter descriptions for SimpleMethod
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)0, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)1, (USHORT)-1 },
{ WS_PARAMETER_TYPE_NORMAL, (USHORT)-1, (USHORT)1 },
},    // parameter descriptions for SimpleMethod
{    // operation description for SimpleMethod
1,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_InputMessage,
(WS_MESSAGE_DESCRIPTION*)&example_wsdl.messages.ISimpleService_SimpleMethod_OutputMessage,
3,
(WS_PARAMETER_DESCRIPTION*)example_wsdlLocalDefinitions.contracts.DefaultBinding_ISimpleService.SimpleMethod.params,
SimpleMethodOperationStub
}, //operation description for SimpleMethod
},  // SimpleMethod
```

<span data-ttu-id="d5176-310">No futuro, ele poderia ser expandido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5176-310">In the future, it could be expanded as follows:</span></span>

``` syntax
WS_OPERATION_DESCRIPTION simpleMethodOperationDesc =
{
  2,
  &ISimpleService_SimpleMethod_InputputMessageDesc,
  &ISimpleService_SimpleMethod_OutputMessageDesc,
  WsCountOf(SimpleMethodParameters),
  SimpleMethodParameters,
  ISimpleService_SimpleMethod_Stub,
  &forwardToString;   // just as an example.
};
```

## <a name="security"></a><span data-ttu-id="d5176-311">Segurança</span><span class="sxs-lookup"><span data-stu-id="d5176-311">Security</span></span>

<span data-ttu-id="d5176-312">Consulte a seção segurança no tópico da [ferramenta do compilador do Wsutil](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="d5176-312">See the security section in the [Wsutil Compiler tool](wsutil-compiler-tool.md) topic.</span></span>

 

 




