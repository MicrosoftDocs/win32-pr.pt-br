---
description: Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma origem de mídia.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Manipuladores de esquema e manipuladores de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7bde81a02762cd9c82e0a7d031582c856da6984ab231775580ddf249caca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058221"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Manipuladores de esquema e manipuladores de Byte-Stream

Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma origem de mídia. Leia este tópico se você estiver implementando uma fonte de mídia personalizada para Media Foundation e desejar que a fonte de mídia esteja disponível para aplicativos por meio do resolvedor de origem.

O resolvedor de origem pode criar uma fonte de mídia de uma URL ou de um fluxo de bytes (ou seja, um ponteiro [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ). Para fazer isso, ele usa objetos auxiliares chamados de *manipuladores*. Para URLs, o resolvedor de origem usa *manipuladores de esquema*. Para fluxos de bytes, ele usa *manipuladores de fluxo de bytes*.

Um manipulador de esquema usa uma URL como entrada e cria uma origem de mídia ou um fluxo de bytes. Se ele criar um fluxo de bytes, o resolvedor de origem irá passá-lo para um manipulador de fluxo de bytes, que cria a origem da mídia. A imagem a seguir ilustra esse processo.

![diagrama mostrando o processo de resolução de origem](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Manipuladores de esquema

Os manipuladores de esquema são usados quando o aplicativo chama [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou seu equivalente assíncrono, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

O resolvedor de origem pesquisa manipuladores de esquema no registro. Os manipuladores de esquema são listados por esquema de URL, sob as seguintes chaves:

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

em que *<scheme>* é o esquema de URL que o manipulador foi projetado para analisar. O esquema inclui o caractere ': ' à direita; por exemplo, "http:".

Para registrar um novo manipulador de esquema, adicione uma entrada cujo nome seja o CLSID do manipulador de esquema, em formato de cadeia de caracteres canônica: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . O valor da entrada é uma cadeia de caracteres (REG \_ SZ) que contém uma breve descrição do manipulador, como "meu manipulador de esquema". A parte importante da entrada é o CLSID. O resolvedor de origem cria o manipulador chamando **CoCreateInstance** com esse CLSID.

Os manipuladores de esquema expõem a interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . Se o resolvedor de origem encontrar um manipulador de esquema que corresponda ao esquema de URL, o resolvedor de origem chamará [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passando a URL original. O manipulador de esquema abrirá a URL e tentará analisar o conteúdo. Nesse ponto, o manipulador de esquema tem duas opções:

-   Crie uma fonte de mídia.
-   Crie um fluxo de bytes.

Se ele criar uma origem de mídia, o resolvedor de origem retornará a origem de mídia para o aplicativo. Se ele criar um fluxo de bytes, o resolvedor de origem tentará localizar um manipulador de fluxo de bytes apropriado, conforme descrito na próxima seção.

## <a name="byte-stream-handlers"></a>Manipuladores de Byte-Stream

Os manipuladores de fluxo de bytes são usados quando o aplicativo chama [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) ou seu equivalente assíncrono, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream). Eles também são usados quando um manipulador de esquema retorna um fluxo de bytes, conforme descrito anteriormente.

Assim como os manipuladores de esquema, os manipuladores de fluxo de bytes são listados no registro. Eles são listados por extensão de nome de arquivo ou tipo MIME (ou ambos), sob as seguintes chaves:

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

em que *<ExtensionOrMimeType>* é a extensão de nome de arquivo ou o tipo MIME. As extensões de arquivo incluem o caractere '. ' inicial; por exemplo, ". wmv".

A extensão de nome de arquivo faz parte da URL, fornecida pelo aplicativo. O tipo MIME pode estar disponível por meio do atributo de [**\_ tipo de \_ conteúdo \_ MF bytes**](mf-bytestream-content-type-attribute.md) no fluxo de bytes.

Para registrar um novo manipulador de fluxo de bytes, adicione uma entrada cujo nome seja o CLSID do manipulador, em formato de cadeia de caracteres canônica. O valor da entrada é uma cadeia de caracteres (REG \_ SZ) que contém uma breve descrição do manipulador, como "meu manipulador de Byte-Stream". O resolvedor de origem chama **CoCreateInstance** para criar o manipulador a partir do CLSID. Você pode registrar o mesmo manipulador em mais de uma extensão ou tipo MIME.

Os manipuladores de fluxo de bytes expõem a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Se o resolvedor de origem encontrar um manipulador de fluxo de bytes correspondente, ele chamará [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). A entrada para esse método é um ponteiro para o fluxo de bytes, além da URL original, se disponível. O manipulador de fluxo de bytes lê a partir do fluxo de bytes até que ele analise dados suficientes para criar a origem da mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 



