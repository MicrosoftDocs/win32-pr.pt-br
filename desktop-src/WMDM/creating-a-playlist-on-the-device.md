---
title: Criando uma lista de reprodução no dispositivo
description: Criando uma lista de reprodução no dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Gerenciador de Dispositivos de mídia do Windows, listas de reprodução
- Gerenciador de Dispositivos, listas de reprodução
- Guia de programação, listas de reprodução
- aplicativos de área de trabalho, listas de reprodução
- criação de aplicativos do Windows Media Gerenciador de Dispositivos, listas de reprodução
- listas de reprodução abstratas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292055"
---
# <a name="creating-a-playlist-on-the-device"></a>Criando uma lista de reprodução no dispositivo

O SDK do Windows Media Gerenciador de Dispositivos fornece os meios para um aplicativo MTP criar uma lista de reprodução em um dispositivo. Esse tipo de lista de reprodução é chamado de lista de reprodução *abstrata* , porque o arquivo criado no dispositivo não contém dados de mídia, mas apenas metadados, que contêm os links para os arquivos de mídia na lista de reprodução.

Outros itens abstratos que podem ser criados no dispositivo incluem álbuns (basicamente listas de reprodução com propriedades extras, como arte de capa), contatos e mensagens.

**Para criar uma lista de reprodução**

1.  Adquira uma interface [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) para o dispositivo de destino.
2.  Chame [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obter a \_ Propriedade g wszWMDMFormatsSupported.
3.  Se não houver suporte para nenhum formato de lista de reprodução, não permita enviar listas de reprodução para o dispositivo e ignore as etapas a seguir. Caso contrário, escolha o código de formato com suporte do dispositivo que corresponda melhor ao tipo de objeto pretendido. Os códigos de \_ formato genérico WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST são os mais comumente suportados.
4.  Obtenha uma interface [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para o armazenamento (a raiz ou uma pasta) em que você deseja criar o objeto. Alguns dispositivos funcionarão melhor se o objeto de playlist for colocado em uma pasta de nível superior chamada "playlists".
5.  Crie um objeto de metadados vazio usando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Usando a interface **IWMDMMetaData** obtida na etapa anterior, chame [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para adicionar o código de formato escolhido (da etapa 3) às propriedades de metadados de armazenamento.
7.  Obtenha a interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) da interface **IWMDMStorage3** .
8.  Chame [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para inserir um novo arquivo de lista de reprodução no armazenamento selecionado. Esse arquivo contém os metadados representados pela interface **IWMDMMetaData** criada na etapa 5 e passados para **Insert3**. O método retorna uma interface **IWMDMStorage** para o arquivo de lista de reprodução; Você pode consultar a interface [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .
9.  Chame [**IWMDMStorage4:: Setreferenciations**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para criar referências às interfaces **IWMDMStorage** dos arquivos de mídia na lista de reprodução.

Para obter um exemplo de código, consulte a \_ função OnCreatePlaylist no [aplicativo de desktop de exemplo](sample-desktop-application.md).

> [!Note]  
> O provedor de serviços MTP fornecido pela Microsoft permite que um aplicativo defina referências em metadados. Para implementar listas de reprodução, seu aplicativo deve estar se comunicando com um dispositivo MTP ou usando um provedor de serviços personalizado que pode manipular objetos abstratos. O provedor de serviços CE manipula a playlist e os objetos de álbum.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




