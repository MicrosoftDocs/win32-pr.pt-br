---
title: Arquivo de extensão de serviço da Web
description: Esta seção descreve o arquivo de extensão de serviço da Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Serviços Web de arquivo de extensão de serviço da Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294619"
---
# <a name="web-service-extension-file"></a>Arquivo de extensão de serviço da Web

Esta seção descreve o arquivo de extensão de serviço da Web.


O arquivo WSX (extensão do serviço WCF) é o nosso arquivo de extensão para permitir que o aplicativo manipule comportamentos locais que não afetam a representação de dados de transmissão. Deve ser extensível para que possamos adicionar novos recursos no futuro sem interromper a interoperabilidade.

A estrutura geral de WSX imitaria a estrutura do arquivo XSD ou WSDL, que é um arquivo XML que mantém a mesma estrutura que o arquivo de entrada principal. Atributos extras no mesmo token nomeado no arquivo principal especificariam os atributos que o aplicativo deseja controlar sobre o comportamento padrão.

Talvez não faça nada aqui em m3. Na V1, posso ver que damos suporte aos seguintes atributos:

Uso especificando o campo de argumento/parâmetro de contagem.

Este é um atributo de elemento, mas aplicável somente ao tipo de matriz. O atributo IsCountOf especifica o elemento da matriz. O parâmetro/campo de contagem não aparece em fio.

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

Esses atributos forçam wsutil.exe a gerar o [**\_ \_ tipo personalizado WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para o tipo especificado. \_o atributo ReadCallback personalizado especifica a rotina de [**retorno de chamada de leitura**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) e WriteCallback personalizado \_ especifica a rotina de [**retorno de chamada de gravação**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .

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

 

 




