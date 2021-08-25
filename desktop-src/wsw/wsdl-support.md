---
title: WSDL e contratos de serviço
description: O utilitário Wsutil.exe gera um stub de linguagem C de acordo com os metadados WSDL fornecidos, bem como definições de tipo de dados e descrições para tipos de dados descritos por esquemas XML de usuário.
ms.assetid: d3c147d6-e370-4e8a-96d8-6660f3a2b996
keywords:
- Suporte a WSDL
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203ee1819a596d2d49a7d0b7c789d5f4e1269b6d8d75f78e2db0913b6a97ec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880736"
---
# <a name="wsdl-and-service-contracts"></a>WSDL e contratos de serviço

O [ utilitárioWsutil.exe](web-service-compiler-tool.md) gera um stub de linguagem C de acordo com os metadados WSDL fornecidos, bem como definições de tipo de dados e descrições para tipos de dados descritos por esquemas XML de usuário.


Veja a seguir um exemplo de documento WSDL e esquema XML que serve como base para a discussão a seguir:

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

Este exemplo fornece um contrato, ISimpleService, com um único método, SimpleMethod. "SimpleMethod" tem dois parâmetros de entrada do tipo **integer**, *a* e *b*, que são enviados do cliente para o serviço. Da mesma forma, SimpleMethod tem dois parâmetros de saída do tipo **inteiro**, *b* e *c*, que são retornados ao cliente após a conclusão bem-sucedida. Na sintaxe C anotada por SAL, a definição do método aparece da seguinte forma:

``` syntax
void SimpleMethod(__in int a, __inout int *  b, __out int * c );
```

Nesta definição, ISimpleService é um contrato de serviço com uma única operação de serviço: SimpleMethod.

O arquivo de header de saída contém definições e descrições para referência externa. Isso inclui:

-   Definições de estrutura C para tipos de elementos globais.
-   Um protótipo de operação conforme definido no arquivo atual.
-   Um protótipo de tabela de funções para os contratos especificados no arquivo WSDL.
-   Protótipos de stub de serviço e proxy de cliente para todas as funções especificadas no arquivo atual.
-   Uma [**estrutura de dados \_ \_ DESCRIÇÃO DO**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) ELEMENTO WS para os elementos de esquema global definidos no arquivo atual.
-   Uma [**estrutura de dados \_ \_ DESCRIÇÃO DA MENSAGEM**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) do WS para todas as mensagens especificadas no arquivo atual.
-   Uma [**estrutura de dados \_ \_ DESCRIÇÃO DO**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) CONTRATO do WS para todos os contratos especificados no arquivo atual.

Uma estrutura global é gerada para encapsular todas as descrições globais para os tipos de esquema e tipos de modelo de serviço aos quais o aplicativo pode se referir. A estrutura é nomeada usando um nome de arquivo normalizado. Neste exemplo, o Wsutil.exe gera uma estrutura de definições globais chamada "wsdl de exemplo" que contém todas as descrições do serviço \_ Web. A definição de estrutura é gerada no arquivo stub.

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

Para definições de elemento global no documento de esquema XML (XSD), um protótipo [**de \_ ELEMENT \_ DESCRIPTION do WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) bem como a definição de tipo C correspondente, são gerados para cada um dos elementos. Os protótipos das descrições de elemento para SimpleMethod e SimpleMethodResponse são gerados como membros na estrutura acima. As estruturas C são geradas da seguinte forma:

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

Da mesma forma, para tipos complexos globais, o Wsutil.exe gera definições de estrutura do tipo C como acima, sem descrições de elemento correspondentes.

Para entrada WSDL, Wsutil.exe gera os seguintes protótipos e definições:

-   Um [**protótipo de \_ DESCRIÇÃO DA MENSAGEM \_ do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) é gerado para a descrição da mensagem. Essa descrição pode ser usada pelo modelo de serviço, bem como pela camada de mensagem. As estruturas de descrição da mensagem são campos chamados "messagename" na estrutura global. Neste exemplo, a descrição da mensagem é gerada como o campo ISimpleService \_ SimpleMethod InputMessage na estrutura \_ ISimpleService \_ SimpleMethod InputMessage, conforme especificado no \_ arquivo WSDL.
-   [**WS \_ O \_ protótipo CONTRACT DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) é gerado para a descrição do contrato. Essa descrição é usada pelo modelo de serviço. As estruturas de descrição do contrato são campos chamados "contractname" na estrutura global. Neste exemplo, a descrição do contrato é gerada como o campo DefaultBinding ISimpleService na estrutura \_ " \_ example \_ wsdl".

As especificações de operação e tipo são comuns a proxy e stub e são geradas em ambos os arquivos. Wsutil.exe gera uma cópia somente se o proxy e o stub são gerados no mesmo arquivo.

## <a name="identifier-generation"></a>Geração de identificador

As estruturas C gerados automaticamente listadas acima são criadas com base no nome especificado no arquivo WSDL. Um NCName XML normalmente não é considerado um identificador C válido e os nomes são normalizados conforme necessário. Os valores hexatórios não são convertidos e letras comuns como ':', '/' e '.' são convertidas no caractere '' sublinhado para melhorar a \_ capacidade de leitura.

## <a name="header-for-the-stub"></a>Header para o stub

Para cada operação no contrato de serviço, uma rotina de retorno de chamada " <operationname> Retorno de chamada" é gerada. (Por exemplo, a operação "SimpleMethod" no contrato de serviço de exemplo tem um retorno de chamada gerado chamado "SimpleMethodCallback".)

``` syntax
typedef HRESULT (CALLBACK *SimpleMethodCallback) (
  const WS_OPERATION_CONTEXT * context,
  int a, int *b, int *c,
  const WS_ASYNC_CONTEXT *asyncContext,
  WS_ERROR * error);
```

Para cada **portType** WSDL, Wsutil.exe gera uma tabela de funções que representa **portType**. Cada operação no **portType** tem um ponteiro de função correspondente para o retorno de chamada presente na tabela de funções.

``` syntax
struct ISimpleServiceMethodTable
{
  ISimpleService_SimpleMethodCallback SimpleMethod;
};
```

Protótipos de proxy são gerados para todas as operações. O nome do protótipo é o nome da operação (nesse caso, "SimpleMethod") especificado no arquivo WSDL para o contrato de serviço.

``` syntax
HRESULT WINAPI SimpleMethod(WS_CHANNEL *channel,
  WS_HEAP *heap,
  int a,
  int *b,
  int *c,
  const WS_ASYNC_CONTEXT * asyncContext,
  WS_ERROR * error );
```

## <a name="local-only-description-prototype-generation"></a>Geração de protótipo de descrição somente local

Os arquivos proxy estub contêm a definição para a estrutura de definições globais, incluindo protótipos e definições para as estruturas que contêm descrições somente locais e implementações de stub de proxy/serviço do cliente.

Todos os protótipos e definições locais para o arquivo stub são gerados como parte de uma estrutura de encapsulamento. Essa estrutura de descrição local abrangente fornece uma hierarquia clara das descrições exigidas pela camada de serialização e pelo modelo de serviço. A estrutura de descrição local tem protótipos semelhantes aos mostrados abaixo:

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

## <a name="referencing-definitions-from-other-files"></a>Referenciando definições de outros arquivos

Definições locais podem referenciar descrições geradas em outro arquivo. Por exemplo, a mensagem pode ser definida no arquivo de código C gerado do arquivo WSDL, mas o elemento de mensagem pode ser definido em outro lugar no arquivo de código C gerado do arquivo XSD. Nesse caso, Wsutil.exe gera referência ao elemento global do arquivo que contém a definição da mensagem, conforme demonstrado abaixo:

``` syntax
{  // WS_MESSAGE_DESCRIPTION
...
(WS_ELEMENT_DESRIPTION *)b_xsd.globalElement.<elementname>
  };
```

## <a name="global-element-descriptions"></a>Descrições de elementos globais

Para cada elemento global definido em um arquivo wsdl:type ou XSD, há um campo correspondente chamado **elementName** dentro do **campo GlobalElement.** Neste exemplo, uma estrutura chamada SimpleMethod é gerada:

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

Outras descrições exigidas pela descrição do elemento são geradas como parte da estrutura que o contém. Se o elemento for um elemento de tipo simples, haverá apenas um [**campo WS \_ ELEMENT \_ DESCRIPTION.**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) Se o tipo de elemento for uma estrutura, todos os campos e descrições de estrutura relacionados serão gerados como parte da estrutura do elemento. Neste exemplo, o elemento SimpleMethod é uma estrutura que contém dois campos, **a e** **b**. Wsutil.exe gera a estrutura da seguinte forma:

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

Estruturas inseridas e elementos inseridos são gerados como sub-estruturas conforme necessário.

## <a name="wsdl-related-definitions"></a>Definições relacionadas ao WSDL

Wsutil.exe gera um campo na seção WSDL para cada um dos valores **portType** definidos no wsdl:service especificado.

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

Wsutil.exe gera um campo f que contém todas as descrições necessárias para a operação, uma matriz de ponteiros para cada uma das descrições da operação para cada método e uma DESCRIÇÃO DE [**CONTRATO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para o **portType especificado.**

Todas as descrições necessárias para operações são geradas dentro do **campo operationName** no **portType especificado.** Eles incluem o campo DESCRIÇÃO DO ELEMENTO [**\_ \_ do WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) bem como a sub-estrutura para os parâmetros de entrada e saída. Da mesma forma, os [**campos DESCRIÇÃO \_ DA MENSAGEM \_ do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) para a mensagem de entrada e a mensagem de saída opcional são incluídos junto com o ; [**WS \_ Campo \_ de**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description) lista PARAMETER DESCRIPTION para todos os parâmetros de operação e o [**campo DESCRIÇÃO DA OPERAÇÃO do WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) para a própria operação. Neste exemplo, a estrutura de código para a descrição simpleMethod é gerada conforme visto abaixo:

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

## <a name="xml-dictionary-related-definitions"></a>Definições relacionadas ao dicionário XML

Nomes e namespaces usados em várias descrições são gerados como campos do tipo [**CADEIA DE CARACTERES \_ XML \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string) Todas essas cadeias de caracteres são geradas como parte de um dicionário constante por arquivo. A lista de cadeias de caracteres e o campo DICIONÁRIO XML do [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary) (chamado **dict** no exemplo abaixo) são gerados como parte do campo de dicionário da estrutura **fileNameLocal.**

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

A matriz de [**CADEIAS DE CARACTERES \_ XML \_ do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)é gerada como uma série de campos do tipo CADEIA DE CARACTERES XML do **WS, \_ \_** nomeados com com nomes amigáveis. O stub gerado usa os nomes amigáveis em várias descrições para melhorar a leitura.

Proxy de cliente para operações WSDL

Wsutil.exe gera um proxy de cliente para todas as operações. Os aplicativos podem substituir a assinatura do método usando uma opção de linha de comando de prefixo.

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

O chamador de operação deve passar um parâmetro *de heap* válido. Os parâmetros de saída são alocados usando o valor heap do WS \_ especificado no parâmetro *heap.* A função de chamada pode redefinir ou liberar o heap para liberar memória para todos os parâmetros de saída. Se a operação falhar, informações de erro de detalhes adicionais poderão ser recuperadas do objeto de erro opcional, se estiver disponível.

Wsutil.exe gera um stub de serviço para todas as operações descritas na associação.

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

A seção acima descreve o protótipo da estrutura local que contém todas as definições locais somente para o arquivo stub. As seções subsequentes descrevem as definições das descrições.

## <a name="wsdl-definition-generation"></a>Geração de definição WSDL

Wsutil.exe gera uma estrutura estática constante (**const static**) chamada<nome de arquivo *\_>* LocalDefinitions do tipo<service *name \_>* Local que contém todas as definições somente locais.

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

Há suporte para as seguintes descrições do WSDL:

-   wsdl:service
-   wsdl:binding
-   wsdl:portType
-   wsdl:operation
-   WSDL: mensagem

## <a name="processing-wsdloperation-and-wsdlmessage"></a>Processando WSDL: Operation e WSDL: Message

Cada operação especificada no documento WSDL é mapeada para uma operação de serviço por [Wsutil.exe](web-service-compiler-tool.md). A ferramenta gera definições separadas das operações de serviço para o servidor e o cliente.

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

O layout dos elementos de dados da mensagem andoutput de entrada é avaliado pela ferramenta para gerar os metadados de serialização para a infraestrutura, juntamente com a assinatura real da operação de serviço resultante à qual as mensagens de entrada e saída estão associadas.

Os metadados de cada operação dentro de um **PortType** específico têm entrada e, opcionalmente, uma mensagem de saída, cada uma dessas mensagens é mapeada para uma [**\_ \_ Descrição de mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description). Neste exemplo, a entrada e a mensagem de saída na operação em portType mapeado para inputMessageDescription e, opcionalmente, o outputMessageDescription na [**Descrição da \_ operação \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) , respectivamente.

Para cada mensagem WSDL, a ferramenta gera a [**\_ \_ Descrição da mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description) que faz referência à definição da [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description) , conforme demonstrado abaixo:

``` syntax
... 
{    // message description for ISimpleService_SimpleMethod_InputMessage
  (WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
  (WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_wsdl.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

A descrição da mensagem refere-se à descrição do elemento de entrada. Como o elemento é definido globalmente, a descrição da mensagem faz referência à definição global em vez do elemento estático local. Da mesma forma, se o elemento for definido em outro arquivo, Wsutil.exe gerará uma referência à estrutura definida globalmente nesse arquivo. Por exemplo, se SimpleMethodResponse for definido em outro arquivo. xsd de exemplo, Wsutil.exe gerará o seguinte em vez disso:

``` syntax
...
{    // message description for ISimpleService_SimpleMethod_InputMessage
(WS_XML_STRING*)&example_wsdlLocalDefinitions.dictionary.xmlStrings.DefaultBinding_ISimpleServiceISimpleService_SimpleMethod_InputMessageactionName,
(WS_ELEMENT_DESCRIPTION*)&(WS_ELEMENT_DESCRIPTION*)&example_xsd.globalElements.SimpleMethodReponse
},  // message description for ISimpleService_SimpleMethod_InputMessage
...
```

Cada descrição da mensagem contém a ação e a descrição do elemento específico (um campo do tipo [**\_ \_ Descrição do elemento WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)) para todos os elementos de dados da mensagem. No caso de uma mensagem em estilo RPC ou uma mensagem com várias partes, um elemento wrapper é criado para encapsular as informações adicionais.

## <a name="rpc-style-support"></a>Suporte ao estilo RPC

Wsutil.exe dá suporte ao estilo de documento, bem como a operações de estilo RPC de acordo com a extensão de associação WSDL 1,1 para a especificação SOAP 1,2. As operações de estilo RPC e literal são marcadas como \_ operação WS RPC \_ literal \_ . O modelo de serviço ignora o nome do elemento wrapper de corpo de resposta em operações RPC/literal.

Wsutil.exe não oferece suporte nativo a operações de estilo de codificação. O \_ parâmetro de buffer XML do WS \_ é gerado para mensagens de codificação e os desenvolvedores devem preencher o buffer opaco diretamente.

## <a name="multiple-message-parts-support"></a>Suporte a várias partes de mensagens

O Wsutil.exe dá suporte a várias partes de mensagem em uma mensagem. Uma mensagem de várias partes pode ser especificada da seguinte maneira:

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

Wsutil.exe gera um campo de [**\_ \_ tipo struct do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para o elemento Message se a mensagem contiver várias partes. Se a mensagem for representada usando o estilo do documento, Wsutil.exe gerará um elemento wrapper com o tipo struct. O elemento wrapper não tem um nome ou um namespace específico, e a estrutura do wrapper contém todos os elementos de todas as partes como campos. O elemento wrapper é somente para uso interno e não será serializado no corpo da mensagem.

Se a mensagem estiver usando a representação de estilo de RPC ou literal, Wsutil.exe criará um elemento wrapper com o nome da operação como o nome do elemento e o namespace especificado como namespace de serviço, de acordo com a especificação de extensão SOAP WSDL. A estrutura do elemento contém uma matriz de campos que representa os tipos especificados nas partes da mensagem. O elemento wrapper é mapeado para o elemento top real no corpo da mensagem, conforme indicado na especificação SOAP.

No lado do servidor, cada operação resulta em um typedef da operação de serviço do servidor resultante. Esse typedef é usado para fazer referência à operação na tabela de funções, conforme descrito anteriormente. Cada operação também resulta na geração de uma função de stub que nfrastructure chamadas em nome do delegado para o método real.

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

Para a operação SimpleMethod, o typedef SimpleMethodOperation é definido acima. Observe que o método gerado tem um argumento expandido listwith a parte da mensagem para a mensagem de entrada e saída para a operação SimpleMethod como parâmetros nomeados.

No lado do cliente, cada operação é mapeada para uma operação de serviço de proxy.

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

## <a name="processing-wsdlbinding"></a>Processando WSDL: Binding

O modelo de serviço WWSAPI dá suporte à extensão de associação SOAP. Para cada associação, há um **PortType** associado.

O transporte especificado na extensão de ligação SOAP é apenas para consultoria. O aplicativo precisa fornecer informações de transporte ao criar um canal. Atualmente, damos suporte à \_ Associação http WS \_ e \_ associações de associação TCP WS \_ .

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

Em nosso documento WSDL de exemplo, temos apenas um **PortType** para ISimpleService. A associação SOAP fornecida indica o transporte HTTP, que é especificado como \_ Associação http WS \_ . Observe que essa estrutura não tem decoração estática, pois essa estrutura precisa estar disponível para o aplicativo.

Processando WSDL: portType

Cada **PortType** no WSDL é constituído de uma ou mais operações. A operação deve ser consistente com a extensão de ligação SOAP indicada em WSDL: Binding.

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

Neste exemplo, o **PortType** ISimpleService contém apenas a operação SimpleMethod. Isso é consistente com a seção de associação em que há apenas uma operação WSDL que é mapeada para uma ação SOAP.

Como o **PortType** ISimpleService tem apenas uma operação--SimpleMethod--a tabela de funções correspondente contém apenas SimpleMethod como uma operação de serviço.

Em termos de metadados, cada **PortType** é mapeado por Wsutil.exe para [**uma \_ \_ Descrição de contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description). Cada operação dentro de um **PortType** é mapeada para [**uma \_ \_ Descrição de operação do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

Neste exemplo, **PortType** a ferramenta gera a [**\_ \_ Descrição do contrato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) para ISimpleService. Esta descrição do contrato contém o número específico de operações disponíveis no **PortType** ISimpleService junto com uma matriz de [**\_ \_ Descrição da operação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) que representa as operações individuais definidas em PortType para ISimpleService. Como há apenas uma operação em portType ISimpleService para ISimpleService, também há apenas uma definição de **\_ \_ Descrição de operação do WS** .

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

## <a name="processing-wsdlservice"></a>Processando WSDL: Service

O WsUtil.exe usa os serviços para encontrar Associação/PortType e gera a estrutura de contrato que descreve tipos, mensagens, definições PortType e assim por diante. As descrições de contrato são acessíveis externamente e são geradas como parte da estrutura de definição global especificada por meio do cabeçalho gerado.

O WsUtil.exe dá suporte a extensões EndpointReference definidas em WSDL: Port. A referência de ponto de extremidade é definida no WS-ADDRESSing como uma maneira de descrever informações de [ponto de extremidade](endpoint-address.md) de um serviço. O texto da extensão de referência do ponto de extremidade de entrada salvo como [**\_ cadeia de \_ caracteres XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string), junto com a descrição correspondente do [**\_ \_ endereço \_ de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description) , é gerado na seção endpointReferences na estrutura global.

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

Para criar [**um \_ \_ endereço de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) usando os metadados gerados pelo WsUtil:

``` syntax
WsCreateReader      // Create a WS_XML_READER
Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput          // Set the encoding and input of the reader to generated endpointReferenceString
WsReadType        // Read WS_ENDPOINT_ADDRESS from the reader
    // Using WS_ELEMENT_TYPE_MAPPING, WS_ENDPOINT_ADDRESS_TYPE and generated endpointAddressDescription, 
```

As cadeias de caracteres constantes no proxy do cliente ou no stub do serviço são geradas como campos do tipo \_ cadeia de caracteres XML do WS \_ , e há um dicionário constante para todas as cadeias de caracteres no arquivo de proxy ou de stub. Cada cadeia de caracteres no dicionário é gerada como um campo na parte de dicionário da estrutura local para melhorar a legibilidade.

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

## <a name="processing-wsdltype"></a>Processando WSDL: Type

Wsutil.exe dá suporte apenas a documentos XSD (esquema XML) em especificação WSDL: Type. Um caso especial é quando uma porta de mensagem Especifica uma definição de elemento global. Consulte a seção a seguir para obter mais detalhes sobre a heurística usada nesses casos.

## <a name="parameter-processing-heuristics"></a>Heurística de processamento de parâmetro

No modelo de serviço, as mensagens WSDL são mapeadas para parâmetros específicos em um método. Wsutil.exe tem dois estilos de geração de parâmetro: no primeiro estilo, a operação tem um parâmetro para a mensagem de entrada e um parâmetro para a mensagem de saída (se necessário); no segundo estilo, Wsutil.exe usa uma heurística para mapear e expandir os campos nas estruturas para mensagens de entrada e mensagens de saída para parâmetros diferentes na operação. As mensagens de entrada e saída precisam ter elementos de mensagem de tipo de estrutura para gerar essa segunda abordagem.

Wsutil.exe usa as seguintes regras ao gerar parâmetros de operação das mensagens de entrada e saída:

-   Para mensagens de entrada e saída com várias partes de mensagem, cada parte de mensagem é um parâmetro separado na operação, com o nome da parte da mensagem como nome do parâmetro.
-   Para a mensagem de estilo RPC com uma parte de mensagem, a parte da mensagem é um parâmetro na operação, com o nome da parte da mensagem como nome do parâmetro.
-   Para mensagens de entrada e saída no estilo de documento com uma parte de mensagem:
    -   Se o nome de uma parte de mensagem for "Parameters" e o tipo de elemento for uma estrutura, cada campo na estrutura será tratado como um parâmetro separado com o nome do campo sendo o nome do parâmetro.
    -   Se o nome da parte da mensagem não for "Parameters", a mensagem será um parâmetro na operação com o nome da mensagem usado como o nome do parâmetro correspondente.
-   Para a mensagem de entrada e saída do estilo do documento com o elemento anulável, a mensagem é mapeada para um parâmetro, com o nome da parte da mensagem como nome do parâmetro. Um nível adicional de indireção é adicionado para indicar que o ponteiro pode ser **nulo**.
-   Se um campo aparecer apenas no elemento de mensagem de entrada, o campo será tratado como \[ um \] parâmetro in.
-   Se um campo aparecer somente no elemento de mensagem de saída, o campo será tratado como \[ um \] parâmetro out.
-   Se houver um campo com o mesmo nome e o mesmo tipo que aparece na mensagem de entrada e na mensagem de saída, o campo será tratado como um \[ parâmetro in e out \] .

As ferramentas a seguir são usadas para determinar a direção dos parâmetros:

-   Se um campo aparecer apenas no elemento de mensagem de entrada, o campo será tratado como somente no parâmetro.
-   Se um campo aparecer apenas no elemento de mensagem de saída, o campo será tratado como somente parâmetro.
-   Se houver um campo com o mesmo nome e o mesmo tipo que aparece na mensagem de entrada e na mensagem de saída, o campo será tratado como um parâmetro in e out.

Wsutil.exe só dá suporte a elementos sequenciados. Ele rejeita a ordenação inválida com relação aos \[ parâmetros de saída \] se Wsutil.exe não pode combinar os parâmetros in e out em uma única lista de parâmetros. Os sufixos podem ser adicionados aos nomes de parâmetro para evitar a colisão de nomes.

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

Wsutil.exe considera os campos em TNS: SimpleMethod e TNS: SimpleMethodResponse ato são parâmetros, como visto nas definições de parâmetro abaixo:

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

Wsutil.exe expande a lista de parâmetros dos campos na lista acima e gera a estrutura **ParamStruct** no exemplo de código a seguir. O tempo de execução do modelo de serviço pode usar essa estrutura para passar argumentos para os stubs do cliente e do servidor.

``` syntax
typedef struct SimpleMethodParamStruct {
  unsigned int   a;  
  unsigned int   b;
  unsigned int   c;
} ;
```

Essa estrutura é usada apenas para descrever o quadro de pilha no cliente e no lado do servidor. Não há nenhuma alteração na descrição da mensagem ou nas descrições de elemento referenciadas pela descrição da mensagem.

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

Como regra geral, um nível de indireção é adicionado para todos os \[ \] parâmetros out e \[ in, out \] .

## <a name="parameterless-operation"></a>Operação sem parâmetros

Para operações de documento e literal, Wsutil.exe trata a operação como tendo um parâmetro de entrada e um parâmetro de saída se:

-   A mensagem de entrada ou saída tem mais de uma parte.
-   Há apenas uma parte da mensagem e o nome da parte da mensagem não é "parâmetros".

.. No exemplo acima, supondo que as partes da mensagem sejam denominadas *ParamIn*" e *ParamOut*, a assinatura do método se torna o seguinte código:

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

Wsutil.exe gera uma assinatura de versão para a descrição da operação, de forma que o mecanismo de modelo de serviço WsCall e do lado do servidor possa verificar se a descrição gerada é aplicável à plataforma atual.

Essas informações de versão são geradas como parte da estrutura [**OPERATION \_ DESCRIPTION \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description) O número de versão pode ser tratado como um seletor de arm de união para tornar a estrutura extensível. Atualmente, a **versionID** é definida como1 sem campos subsequentes. Os versiosn futuros podem incrementar o número de versão e incluir mais campos conforme necessário. Por exemplo, Wsutil.exe atualmente gera o seguinte código com base na ID da versão:

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

No futuro, ele pode ser expandido da seguinte forma:

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

## <a name="security"></a>Segurança

Consulte a seção de segurança no tópico [ferramenta do Compilador Wsutil.](wsutil-compiler-tool.md)

 

 




