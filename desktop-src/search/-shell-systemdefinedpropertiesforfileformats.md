---
description: O Microsoft Windows fornece várias propriedades do sistema que você pode usar para seus formatos de arquivo.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Propriedades de System-Defined para formatos de arquivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090055"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>Propriedades de System-Defined para formatos de arquivo personalizados

O Microsoft Windows fornece várias propriedades do sistema que você pode usar para seus formatos de arquivo. Se você estiver criando um formato de arquivo personalizado, deverá oferecer suporte a tantas propriedades definidas pelo sistema quanto possível. Antes de criar um manipulador de propriedade personalizada, você deve revisar os manipuladores fornecidos pelo sistema para ver se você pode usar um em vez de escrever o seu próprio.

A tabela a seguir categoriza os formatos de arquivo e lista as propriedades de sistema mais importantes às quais o formato de arquivo deve dar suporte. Para fornecer uma boa experiência do usuário, você deve dar suporte a todas as propriedades de prioridade 1 e 2 para sua categoria de formato de arquivo.

-   [Comunicações](#communications)
-   [Contatos](#contacts)
-   [Documentos](#documents)
-   [Genérico](#generic)
-   [Música](#music)
-   [Imagens](#pictures)
-   [Vídeos](#videos)
-   [Tópicos relacionados](#related-topics)

## <a name="communications"></a>Comunicações



| Nome            | Propriedade                               | Prioridade |
|-----------------|----------------------------------------|----------|
| Data de recebimento   | System. Message. DateReceived            | 1        |
| Nomes de      | System. Message. FromName                | 1        |
| Tem anexos | System. Message. HasAttachments          | 1        |
| Mailbox         | System. Communication. storeddisplayname | 1        |
| Name            | System. FileName                        | 1        |
| Assunto         | Sistema. Subject                         | 1        |
| Nomes para        | System. Message. NoName                  | 1        |
| Categoria        | System. Category                        | 2        |
| Tipo            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contatos



| Nome             | Propriedade                           | Prioridade |
|------------------|------------------------------------|----------|
| Nome da Conta     | System. Communication. AccountName   | 1        |
| Telefone comercial   | System. Contact. BusinessTelephone   | 1        |
| Empresa          | System. Company                     | 1        |
| Endereço de Email    | System. Contact. PrimaryEmailAddress | 1        |
| Importância       | System. ImportanceText              | 1        |
| Telefone celular     | System. Contact. MobileTelephone     | 1        |
| Endereço comercial | System. Contact. BusinessAddress     | 2        |
| Fax comercial     | System. Contact. BusinessFaxNumber   | 2        |
| Categoria         | System. Category                    | 2        |
| Endereço residencial     | System. Contact. HomeAddress         | 2        |
| Telefone residencial       | System. Contact. HomeTelephone       | 2        |
| Título            | System.Title                       | 2        |



 

## <a name="documents"></a>Documentos



| Nome      | Propriedade             | Prioridade |
|-----------|----------------------|----------|
| Autores   | System.Author        | 1        |
| Texto Completo | Sistema. FullText      | 1        |
| Marcas      | System.Keywords      | 1        |
| Tipo      | System.PerceivedType | 1        |
| Categoria  | System. Category      | 2        |
| Título     | System.Title         | 2        |



 

## <a name="generic"></a>Genérico



| Nome     | Propriedade             | Prioridade |
|----------|----------------------|----------|
| Autores  | System.Author        | 1        |
| Título    | System.Title         | 1        |
| Tipo     | System.PerceivedType | 1        |
| Categoria | System. Category      | 2        |
| Marcas     | System.Keywords      | 2        |



 

## <a name="music"></a>Música



| Nome         | Propriedade                     | Prioridade |
|--------------|------------------------------|----------|
| \#           | System. Music. TrackNumber     | 1        |
| Álbuns        | System. Music. campos AlbumTitle      | 1        |
| Artistas      | System. Music. artista          | 1        |
| Gênero        | System. Music. Gênero           | 1        |
| Classificação       | System. rating                | 1        |
| Título        | System.Title                 | 1        |
| Artista do álbum | System. Music. AlbumArtist     | 2        |
| Taxa de bits     | System. Audio. EncodingBitrate | 2        |
| Condutores   | Sistema. Music. condutor       | 2        |
| Comprimento       | System. Media. Duration        | 2        |
| Protegido    | System. DRM. isproteged       | 2        |
| Year         | Sistema. Media. Year            | 2        |



 

## <a name="pictures"></a>Imagens



| Nome          | Propriedade                        | Prioridade |
|---------------|---------------------------------|----------|
| Data de importação | System. DateImported             | 1        |
| Data de início    | System. Photo. DateTaken          | 1        |
| Classificação        | System. rating                   | 1        |
| Marcas          | System.Keywords                 | 1        |
| Tipo          | System.PerceivedType            | 1        |
| Autores       | System.Author                   | 2        |
| Criador de câmera  | System. Photo. CameraManufacturer | 2        |
| Modelo de câmera  | System. Photo. CameraModel        | 2        |
| Comentários      | Sistema. Comment                  | 2        |
| Dimensões    | System. Image. Dimensions         | 2        |



 

## <a name="videos"></a>Vídeos



| Nome         | Propriedade                 | Prioridade |
|--------------|--------------------------|----------|
| Comprimento       | System. Media. Duration    | 1        |
| Classificação       | System. rating            | 1        |
| Marcas         | System.Keywords          | 1        |
| Tipo         | System.PerceivedType     | 1        |
| Altura do quadro | System. vídeo. FrameHeight | 2        |
| Largura do quadro  | System. vídeo. FrameWidth  | 2        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Desenvolvendo manipuladores de propriedade para o Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Sistema de propriedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
