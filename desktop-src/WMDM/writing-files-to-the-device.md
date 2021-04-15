---
title: Gravando arquivos no dispositivo
description: Gravando arquivos no dispositivo
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media Gerenciador de Dispositivos, gravando arquivos em dispositivos
- Gerenciador de Dispositivos, gravando arquivos em dispositivos
- Guia de programação, gravando arquivos em dispositivos
- aplicativos de área de trabalho, gravando arquivos em dispositivos
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, gravando arquivos em dispositivos
- gravando arquivos em dispositivos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498615"
---
# <a name="writing-files-to-the-device"></a>Gravando arquivos no dispositivo

Antes de enviar um arquivo para um dispositivo, seu aplicativo deve descobrir quais tipos de arquivos e formatos o dispositivo pode manipular, para que o aplicativo possa determinar se o arquivo deve ser transcodificado antes do envio ou enviado não modificado ou não enviado.

As etapas a seguir mostram como enviar um arquivo existente para o dispositivo. Para criar um novo arquivo no dispositivo, como uma lista de reprodução, consulte [criando uma lista de reprodução no dispositivo](creating-a-playlist-on-the-device.md).

1.  Obtenha o formato do arquivo que você pretende enviar para o dispositivo. Para obter mais informações, consulte [descobrindo o formato de um arquivo](discovering-a-files-format.md).
2.  Se o dispositivo for destinado a executar o arquivo,
    -   Consulte o arquivo para obter seus recursos de formato. Para obter mais informações, consulte [descobrindo recursos de formato de dispositivo](discovering-device-format-capabilities.md).
    -   Localize um formato aceitável que o aplicativo possa criar a partir do arquivo original.
    -   Se o arquivo precisar ser transcodificado, transcodifique-o.
3.  Localize um armazenamento pai para o novo objeto. O Windows Media Gerenciador de Dispositivos não fornece uma maneira de descobrir o local de armazenamento padrão para qualquer tipo de arquivo específico (arquivos de vídeo ou áudio, WMV ou BMP, uma pasta "favoritos" e assim por diante), portanto, você precisará examinar cada dispositivo para tentar descobrir onde melhor armazenar o novo objeto. (Outros aplicativos impõem uma determinada estrutura de pastas, por exemplo, o Windows Media Player cria álbuns, listas de reprodução e pastas de músicas em que a pasta música contém uma hierarquia de artista e Álbumname. Por esse motivo, e como alguns dispositivos podem não ter sido testados com software diferente do Windows Media Player, lembre-se de que o posicionamento de objetos de lista de reprodução ou de álbuns em qualquer pasta diferente das pastas playlists ou álbuns pode, às vezes, levar a objetos que não funcionam em alguns dispositivos.)
4.  Se o armazenamento de destino der suporte a [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), crie uma nova interface de metadados chamando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Defina os metadados em uma interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) . Para obter mais informações, consulte [definindo metadados em um arquivo](setting-metadata-on-a-file.md). Os únicos metadados necessários são g \_ wszWMDMFormatCode (um valor de [**\_ FORMATCODE de WMDM**](wmdm-formatcode.md) que descreve o conteúdo), mas quanto mais metadados você puder fornecer, mais eficiente será a transferência para o provedor de serviços.
5.  Envie o arquivo para o dispositivo usando o método [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)ou [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) . O **Insert3** permite que você inclua os metadados no dispositivo como parte do método. Para obter mais informações, consulte [enviando o arquivo para o dispositivo](sending-the-file-to-the-device.md).

O código que demonstra cada uma dessas etapas é fornecido nas páginas de tópico vinculadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




