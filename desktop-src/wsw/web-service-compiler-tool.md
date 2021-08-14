---
title: Ferramenta de compilador de serviço Web
description: Para dar suporte ao modelo de serviço, wsutil.exe gera o cabeçalho a ser usado no lado do cliente e do serviço. Ele gera o arquivo de proxy C para o lado do cliente e o arquivo stub C para o lado do serviço, conforme necessário.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Serviços Web da ferramenta de compilador de serviço Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92e1195cd9d3a8e8d9fa1b7be94421d68f3cbdf2242be6fa0d05be5cc3c743f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962835"
---
# <a name="web-service-compiler-tool"></a>Ferramenta de compilador de serviço Web

Para dar suporte ao modelo de serviço, wsutil.exe gera o cabeçalho a ser usado no lado do cliente e do serviço. Ele gera o arquivo de proxy C para o lado do cliente e o arquivo stub C para o lado do serviço, conforme necessário.


Para dar suporte à [serialização](serialization.md), o compilador gera cabeçalhos para descrições de elemento para definições de elementos globais e todas as informações de definição de tipo no arquivo de proxy a serem consumidas pelo mecanismo de serialização.

Uso

**Opções de opção de linha de comando deWsUtil.exe \[ \[ \] :\]<filename>**

opções de linha de comando

Especifica WsUtil.exe opções do compilador. As opções podem aparecer em qualquer ordem. Dash ('-') e barra ('/') são tratados como o mesmo.

Lista de opções de linha de comando

-   @filename Especifica que o arquivo de entrada deve ser tratado como um arquivo de resposta. Essa opção pode ser usada várias vezes, em qualquer lugar na lista de argumentos.
-   /WSDL: <filename> : <\_ url opcional> especifica que o arquivo de entrada deve ser tratado como um arquivo WSDL. Várias entradas WSDL são permitidas e todos os arquivos WSDL especificados são processados. A \_ URL opcional especifica o local do qual os metadados foram recuperados. Se nenhuma \_ URL opcional for especificada, Wsutil gerará uma URL exclusiva internamente. Consulte também [suporte a políticas](policy-support.md).
-   /xsd: <filename> especifica que o nome de arquivo de entrada deve ser tratado como um arquivo de esquema. Várias entradas XSD são permitidas e todos os arquivos de esquema especificados são processados.
-   /WSP: <filename> : <\_ url opcional> especifica que o nome de arquivo de entrada deve ser tratado como metadados de política. Várias entradas WSP são permitidas e todos os arquivos de política especificados são processados. A \_ URL opcional especifica o local do qual os metadados foram recuperados. Se nenhuma \_ URL opcional for especificada, Wsutil gerará uma URL exclusiva internamente. Os arquivos de política serão ignorados se o sinalizador/nopolicy for especificado. Consulte também [suporte a políticas](policy-support.md).
-   /nopolicy desabilitar o processamento de política.
-   /out: <dirname> especifica o nome do diretório para arquivos de saída
-   /noclient não geram o stub do lado do cliente.
-   /noservice não geram o stub do lado do serviço.
-   /prefix: <string> preceder a cadeia de caracteres especificada para todos os identificadores gerados.
-   /FullName preceda o nome de arquivo normalizado para identificadores gerados. Por padrão, somente o nome especificado no atributo "Name" será usado para gerar identificadores para descrições relacionadas.
-   /String: <WS \_ string>\|<WCHAR \*> por padrão, Wsutil gera WCHAR \* para o tipo xsd: String. O aplicativo pode usar esse sinalizador para substituir esse comportamento e gera a \_ cadeia de caracteres WS para xsd: Type.
-   /Help exibir mensagem de ajuda
-   /? Mesmo que/Help
-   /W: x opções de tratamento de erros. Poderia ser W:0-W: 4 \| WX
-   /nologo não gere informações específicas do compilador na saída do console.
-   /nostamp não gere informações específicas do compilador em arquivos gerados.

Por padrão, o compilador gera os seguintes arquivos para o arquivo WSDL ou o WSDL retornado da troca de metadados:

-   Proxy do cliente ({inputfilename}. c)
-   Stub de serviço ({inputfilename}. c)
-   Arquivo de cabeçalho ({inputfilename}. h)

    A raiz do filename gerado é o nome do arquivo de entrada. As extensões de arquivo de entrada originais são preservadas para evitar a colisão de nome de arquivo para arquivos gerados. Por padrão, os stubs de serviço e cliente são gerados no mesmo arquivo, com o código stub de serviço gerado após o código de proxy.

    Por padrão, o compilador gera os seguintes arquivos para um arquivo XSD para o esquema retornado da troca de metadados:

-   descrições de serialização ({inputfilename}. c)
-   Arquivo de cabeçalho ({inputfilename}. h)

    A raiz do nome do arquivo é o nome do serviço.

Wsutil.exe gera uma seção "Stamp" no início de todos os arquivos gerados, indicando a opção do compilador, a versão da ferramenta, a opção de linha de comando aplicável, etc. Esta seção pode ser desativada usando a opção/nostamp para evitar ruídos com a comparação de arquivos gerados.

Wsutil não dá suporte ao download de metadados

O compilador Wsutil funciona somente do arquivo de metadados local. A ferramenta não oferece suporte ao download de metadados de serviços Web em execução. Os desenvolvedores podem usar outras ferramentas WebService com suporte, como SvcUtil, para baixar metadados para o computador local, inspecionar os arquivos salvos e passar esses arquivos para wsutil.exe para compilação.

Suporte a vários arquivos de entrada/saída

O esquema WSDL e XML permite incluir/importar definições de outros espaços de nome especificados em outros locais/arquivos. O Wsutil dá suporte a várias entradas de esquema/WSDL/política e gera um conjunto de stub/cabeçalho para cada arquivo de entrada. O Wsutil não segue as instruções include e Import. Em vez disso, o aplicativo deve passar arquivos que contenham todos os namespaces necessários para Wsutil, de modo que a ferramenta possa resolver todas as dependências durante a compilação.

**WsUtil.exe/xsd: StockQuote. XSD/WSDL: StockQuote. WSDL/WSDL: StockQuoteService. WSDL**

o Wsutil gera três conjuntos de arquivos de saída:

-   StockQuote. xsd. c StockQuote. xsd. h
-   StockQuote. WSDL. c StockQuote. WSDL. h
-   StockQuoteService. WSDL. h stockquoteservices. WSDL. c

Formato do arquivo de saída

Para cada arquivo de saída, o Wsutil gera definições externas disponíveis no arquivo de cabeçalho. Além de definições de estrutura C e protótipos de função de stub, todas as outras definições relacionadas a serviços Web são encapsuladas em uma estrutura global chamada com nome de arquivo normalizado.

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

Observe que nem todos os campos são gerados para a estrutura global. Um campo de nível superior é gerado somente quando as definições relacionadas são especificadas no arquivo de entrada. Por exemplo, nenhum campo de mensagem, operações e contratos é gerado para arquivos XSD.

Níveis de aviso e nível de erro

Semelhante ao compilador C, o WsUtil.exe dá suporte a quatro níveis de aviso e um nível de erro:

-   WsUtil.exe gera erros com falhas irrecuperáveis, como arquivo WSDL inválido, opções de compilador inválidas etc.
-   O WsUtil gera avisos de W1 com sérios problemas recuperáveis. O compilador pode continuar, mas o usuário deve estar ciente do problema. Por exemplo, um aviso de W1 será gerado se houver atributos sem suporte, como algumas facetas WSDL, em WSDL que não afetam a geração de código.
-   O WsUtil gera avisos de W2 com problemas menos graves. Não há perda de funcionalidade, mas o desenvolvedor de aplicativos pode querer saber isso. Como comportamentos que podem ser diferentes de outras plataformas.
-   O WsUtil gera avisos w3 com impacto mínimo sobre o código gerado. Por exemplo, wsutil.exe gera um aviso w3 quando a cadeia de caracteres normalizada é diferente da cadeia de caracteres original.
-   O erro de W4 é mais semelhante aos avisos "informativos" e WsUtil o W4, em casos como ignorar o atributo de documentação no WSDL.
-   O WX indica que o compilador trata o aviso como erro. Por exemplo, Wsutil gerará um erro para todos os avisos de W1 se/W: 1/WX for especificado.

/W: {N} especifique qual nível de mensagem de aviso deve ser gerado. /W: 1 significa que os avisos do nível de aviso 1 devem ser gerados e os avisos do nível de aviso 2 e inferior devem ser mascarados e não gerados pela ferramenta.

## <a name="fullname"></a>/fullname

Essa opção indica que WsUtil.exe gera um nome completo para identificadores para evitar a possível colisão de nomes. Por exemplo, no example. xsd temos:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

Por padrão, o WsUtil.exe gera:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Mas se a opção de linha de comando/FullName for especificada, WsUtil.exe gerará a seguinte definição de estrutura em vez disso:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalização

A ferramenta é neutra de idioma e pode ser localizada em idiomas diferentes. Todas as mensagens de erro/saída do console podem ser localizadas. No entanto, as opções de linha de comando permanecem em inglês.

## <a name="environment-variable"></a>Variável de ambiente

WsUtil.exe não usa nenhuma variável de ambiente.

## <a name="platform-independent"></a>Independente de plataforma

Os arquivos de saída de WsUtil.exe são independentes de plataforma. Não há código dependente de arquitetura gerado no stub; qualquer outra arquitetura específica será encarregada pelo compilador do C. O stub pode ser usado em todas as plataformas às quais damos suporte.

A descrição de wsutil.exe saída pode ser encontrada em [suporte WSDL](wsdl-support.md) e parte de [suporte do esquema](schema-support.md) .

 

 




