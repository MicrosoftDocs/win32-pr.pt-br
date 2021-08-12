---
title: Criando uma playlist no dispositivo
description: Criando uma playlist no dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Mídia Gerenciador de Dispositivos, playlists
- Gerenciador de Dispositivos, playlists
- guia de programação, playlists
- aplicativos da área de trabalho, playlists
- criando Windows mídia Gerenciador de Dispositivos aplicativos, playlists
- playlists abstratas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a61d45c234f1cdbe03a713e4d10568fa45c83bdd90227b815c85b0f544d2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585852"
---
# <a name="creating-a-playlist-on-the-device"></a>Criando uma playlist no dispositivo

O SDK Windows Media Gerenciador de Dispositivos fornece os meios para um aplicativo MTP criar uma playlist em um dispositivo. Esse tipo de playlist  é chamado de playlist abstrata, porque o arquivo criado no dispositivo não contém dados de mídia, mas apenas metadados, que contém os links para arquivos de mídia na playlist.

Outros itens abstratos que podem ser criados no dispositivo incluem álbums (essencialmente playlists com propriedades extras, como arte de cobertura), contatos e mensagens.

**Para criar uma playlist**

1.  Adquira uma interface [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) para o dispositivo de destino.
2.  Chame [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obter a propriedade g \_ wszWMDMFormatsSupported.
3.  Se nenhum formato de playlist tiver suporte, não permitirá o envio de playlists para o dispositivo e ignore as etapas a seguir. Caso contrário, escolha o código de formato com suporte do dispositivo que corresponde mais próximo ao tipo de objeto pretendido. Os códigos de formato GENERIC WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST são os mais comumente suportados.
4.  Obtenha uma interface [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para o armazenamento (a raiz ou uma pasta) na qual você deseja criar o objeto. Alguns dispositivos funcionarão melhor se o objeto de playlist for colocado em uma pasta de nível superior chamada "Playlists".
5.  Crie um objeto de metadados vazio usando [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Usando a interface **IWMDMMetaData** obtida na etapa anterior, chame [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para adicionar o código de formato escolhido (da etapa 3) às propriedades de metadados de armazenamento.
7.  Obtenha a interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) da interface **IWMDMStorage3.**
8.  Chame [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para inserir um novo arquivo de playlist no armazenamento selecionado. Esse arquivo contém os metadados representados pela interface **IWMDMMetaData** criada na etapa 5 e passada para **Insert3.** O método retorna uma interface **IWMDMStorage** para o arquivo de playlist; você pode consultar a interface [**IWMDMStorage4.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)
9.  Chame [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para criar referências às interfaces **IWMDMStorage** dos arquivos de mídia na playlist.

Para código de exemplo, consulte a \_ função OnCreatePlaylist no [Aplicativo de Área de Trabalho de Exemplo](sample-desktop-application.md).

> [!Note]  
> O provedor de serviços MTP fornecido pela Microsoft permite que um aplicativo de definir referências em metadados. Para implementar playlists, seu aplicativo deve estar se comunicando com um dispositivo MTP ou usando um provedor de serviços personalizado que possa manipular objetos abstratos. O provedor de serviços CE lida com objetos de playlist e de álbum.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




