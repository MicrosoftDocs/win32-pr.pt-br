---
title: Arquivo de extensão de serviço Web
description: Esta seção descreve o arquivo de extensão do Serviço Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Serviços Web de Arquivo de Extensão de Serviço Web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b11e8e871399e1a499a6cfbb68a8e66b152d8f07f4fa5f2cda6585678af8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707226"
---
# <a name="web-service-extension-file"></a>Arquivo de extensão de serviço Web

Esta seção descreve o arquivo de extensão do Serviço Web.


O arquivo WSX (extensão de serviço WCF) é nosso arquivo de extensão para permitir que o aplicativo manipule comportamentos locais que não afetam a representação de dados de transmissão. Deve ser extensível que possamos adicionar novos recursos no futuro sem a interoperabilidade da quebra.

A estrutura geral do WSX imitaria a estrutura do arquivo XSD ou WSDL, que é um arquivo XML que mantém a mesma estrutura que o arquivo de entrada principal. Atributos extras no mesmo token nomeado no arquivo principal especificariam os atributos que o aplicativo deseja controlar sobre o comportamento padrão.

Talvez não façamos nada aqui no M3. Na V1, posso ver que damos suporte aos seguintes atributos:

Uso Especificando o campo de argumento/parâmetro de contagem.

Esse é um atributo de elemento, mas aplicável somente ao tipo de matriz. O atributo IsCountOf especifica o elemento de matriz. O campo/parâmetro de contagem não aparece na transmissão.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

Especificando o retorno de chamada de leitura/gravação para o tipo personalizado

Esses atributos forçam wsutil.exe a [**gerar O TIPO PERSONALIZADO \_ \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para o tipo especificado. O atributo readcallback personalizado especifica a rotina de retorno de chamada de leitura \_ e writecallback personalizado especifica a rotina de retorno de chamada [](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) \_ [**de**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) gravação.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Podemos ter um arquivo WSX correspondente para descrever seu comportamento local:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe gera o seguinte protótipo para a estrutura:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




