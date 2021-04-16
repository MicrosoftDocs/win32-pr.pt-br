---
description: Atributos de fluxo de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de fluxo de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761145"
---
# <a name="byte-stream-attributes"></a>Atributos de fluxo de bytes

Os atributos a seguir se aplicam a alguns fluxos de bytes. Para descobrir se um fluxo de bytes dá suporte a atributos, consulte o objeto de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Atributo                                                                                  | Descrição                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**\_tipo de \_ conteúdo \_ bytes MF**](mf-bytestream-content-type-attribute.md)              | Especifica o tipo MIME de um fluxo de bytes.                         |
| [**\_duração de bytes MF \_**](mf-bytestream-duration-attribute.md)                       | Especifica a duração de um fluxo de bytes, em unidades de 100 a nanossegundos. |
| [\_URI do arquivo MF bytes \_ IFO \_ \_](mf-bytestream-ifo-file-uri.md)                           | Especifica a URL de um arquivo IFO associado.                      |
| [**\_hora da \_ última \_ modificação \_ do MF bytes**](mf-bytestream-last-modified-time-attribute.md) | Especifica quando um fluxo de bytes foi modificado pela última vez.                   |
| [**nome da origem do MF \_ bytes \_ \_**](mf-bytestream-origin-name-attribute.md)                | Especifica a URL original para um fluxo de bytes.                     |



 

Os atributos a seguir se aplicam a manipuladores de fluxo de bytes.



| Atributo                                                                                    | Descrição                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ aceita \_ gravação de compartilhamento \_](mf-bytestreamhandler-accepts-share-write.md) | Especifica se um manipulador de fluxo de bytes pode usar um fluxo de bytes que é aberto para gravação por outro thread |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



