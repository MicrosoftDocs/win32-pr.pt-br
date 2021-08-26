---
description: Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma fonte de mídia.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Manipuladores de esquema e Byte-Stream manipuladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5cbb2ee0af93e456e86b6eab16ff44705f5380
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881775"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Manipuladores de esquema e Byte-Stream manipuladores

Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma fonte de mídia. Leia este tópico se você estiver implementando uma fonte de mídia personalizada para Media Foundation e quiser que a fonte de mídia seja disponibilizada para aplicativos por meio do resolvedor de origem.

O resolvedor de origem pode criar uma fonte de mídia de uma URL ou de um fluxo de byte (ou seja, um [**ponteiro IMFByteStream).**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) Para fazer isso, ele usa objetos auxiliares chamados *manipuladores*. Para URLs, o resolvedor de origem usa *manipuladores de esquema*. Para fluxos de byte, ele usa *manipuladores de fluxo de byte*.

Um manipulador de esquema recebe uma URL como entrada e cria uma fonte de mídia ou um fluxo de byte. Se ele criar um fluxo de byte, o resolvedor de origem o passará para um manipulador de fluxo de byte, que cria a fonte de mídia. A imagem a seguir ilustra esse processo.

![diagrama mostrando o processo de resolução de origem](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Manipuladores de esquema

Manipuladores de esquema são usados quando o aplicativo chama [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou seu equivalente assíncrono, [**BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)

O resolvedor de origem procura manipuladores de esquema no Registro. Os manipuladores de esquema são listados por esquema de URL, nas seguintes chaves:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

em *&lt; que scheme &gt;* é o esquema de URL que o manipulador foi projetado para analisar. O esquema inclui o caractere ':' à parte final; por exemplo, "http:".

Para registrar um novo manipulador de esquema, adicione uma entrada cujo nome é o CLSID do manipulador de esquema, no formato de cadeia de caracteres canônica: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . O valor da entrada é uma cadeia de caracteres (REG SZ) que contém uma breve descrição do manipulador, como \_ "Meu Manipulador de Esquema". A parte importante da entrada é a CLSID. O resolvedor de origem cria o manipulador chamando **CoCreateInstance** com essa CLSID.

Manipuladores de esquema expõem a interface [**IMFSchemeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) Se o resolvedor de origem encontrar um manipulador de esquema que corresponde ao esquema de URL, o resolvedor de origem chamará [**IMFSchemeHandler::BeginCreateObject,**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)passando a URL original. O manipulador de esquema abrirá a URL e tentará analisar o conteúdo. Nesse ponto, o manipulador de esquema tem duas opções:

-   Criar uma fonte de mídia.
-   Crie um fluxo de byte.

Se ele criar uma fonte de mídia, o resolvedor de origem retornará a fonte de mídia para o aplicativo. Se ele criar um fluxo de byte, o resolvedor de origem tentará encontrar um manipulador de fluxo de byte apropriado, conforme descrito na próxima seção.

## <a name="byte-stream-handlers"></a>manipuladores Byte-Stream dados

Manipuladores de fluxo de byte são usados quando o aplicativo chama [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) ou seu equivalente assíncrono, [**BeginCreateObjectFromByteStream.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) Eles também são usados quando um manipulador de esquema retorna um fluxo de byte, conforme descrito anteriormente.

Assim como com manipuladores de esquema, manipuladores de fluxo de byte são listados no Registro. Eles são listados por extensão de nome de arquivo ou tipo MIME (ou ambos), sob as seguintes chaves:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

em *&lt; que ExtensionOrMimeType é &gt;* a extensão de nome de arquivo ou o tipo MIME. As extensões de arquivo incluem o caractere '.' inicial; por exemplo, ".wmv".

A extensão de nome de arquivo faz parte da URL, fornecida pelo aplicativo. O tipo MIME pode estar disponível por meio do atributo [**\_ MF BYTESTREAM \_ CONTENT \_ TYPE**](mf-bytestream-content-type-attribute.md) no fluxo de byte.

Para registrar um novo manipulador de fluxo de byte, adicione uma entrada cujo nome é o CLSID do manipulador, em formato de cadeia de caracteres canônica. O valor da entrada é uma cadeia de caracteres (REG SZ) que contém uma breve descrição do manipulador, como "Meu manipulador \_ Byte-Stream". O resolvedor de origem chama **CoCreateInstance** para criar o manipulador do CLSID. Você pode registrar o mesmo manipulador em mais de uma extensão ou tipo MIME.

Manipuladores de fluxo de byte expõem a interface [**IMFByteStreamHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) Se o resolvedor de origem encontrar um manipulador de fluxo de byte correspondente, ele chamará [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). A entrada para esse método é um ponteiro para o fluxo de byte, mais a URL original, se disponível. O manipulador de fluxo de byte lê do fluxo de byte até analisar dados suficientes para criar a fonte de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolvedor de Origem](source-resolver.md)
</dt> </dl>

 

 



