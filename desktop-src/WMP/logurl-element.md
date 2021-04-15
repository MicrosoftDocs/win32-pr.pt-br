---
title: Elemento LOGURL
description: O elemento LOGURL instrui o Windows Media Player a enviar quaisquer dados de log para a URL especificada.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Elemento LOGURL do Windows Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761261"
---
# <a name="logurl-element"></a>Elemento LOGURL

O elemento **LogURL** instrui o Windows Media Player a enviar quaisquer dados de log para a URL especificada.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para um host que é capaz de processar solicitações de registro em log.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **ASX**, **entrada** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

O elemento **LogURL** permite que uma lista de reprodução de metarquivo de cliente envie informações de log adicionais para os servidores especificados. As informações de log são enviadas automaticamente ao servidor de origem de uma lista de reprodução quando ela é aberta e a cada **LogURL** especificada para o elemento **ASX** , se houver alguma. As informações de log também são enviadas para cada **LogURL** especificado para um elemento de **entrada** quando essa entrada é atingida. A URL especificada no atributo **href** de um elemento **LogURL** deve ser o endereço de um host capaz de processar solicitações de registro em log. A URL pode ser qualquer URL HTTP válida. A URL também pode indicar o local de um script CGI.

Os únicos protocolos válidos para um elemento **LogURL** são http e HTTPS.

Um elemento **LogURL** dentro do escopo de um elemento **ASX** é aplicável somente ao metarquivo no qual ele reside, independentemente de o metarquivo ser referenciado de outro metarquivo. Um elemento **LogURL** força o envio de dados de log para todo o conteúdo transmitido de dentro de seu escopo definido e apenas para o conteúdo transmitido de dentro de seu escopo definido. Os dados de log serão enviados para o servidor de origem e para todas as URLs listadas em todos os elementos **LogURL** no escopo. Os dados de log serão enviados apenas uma vez para cada URL listada, mesmo que a mesma URL esteja listada mais de uma vez em um determinado escopo. Uma repetição de uma **entrada** resultaria em outro envio às URLs listadas.

Não há nenhum limite para o número de elementos **LogURL** em uma playlist de metarquivo.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



Veja a seguir exemplos de URLs válidas.

URL de um aplicativo ISAPI:


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



URL de um script CGI:


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



Uma URL HTTP válida:


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





