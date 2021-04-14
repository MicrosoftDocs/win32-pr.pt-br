---
title: Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados
description: Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, metadados
- Windows Media Player, transferência de metadados acelerada
- Windows Media Player, transferência acelerada de metadados
- metadados, extensões de dispositivo
- metadados, extensões
- extensões de dispositivo, transferência de metadados
- extensões, transferência de metadados
- transferência de metadados acelerada
- metadados, transferência acelerada
- extensões de dispositivo, transferência de metadados acelerada
- extensões, transferência de metadados acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453645"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados

Para habilitar a transferência de metadados acelerada, os fabricantes de dispositivos que não dão suporte a MTP devem fazer o seguinte no código-fonte:

-   Defina **o \_ \_ \_ suporte ao dispositivo WMDM do WMP**.
-   Inclua wmpdevices. h, que é instalado como parte do SDK do Windows Media Player.

Wmpdevices. h define as estruturas a seguir.



| Estrutura                                                                                 | Descrição                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_PC2DEVICE de \_ \_ viagem de \_ ida \_ e volta de metadados do WMP](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Estrutura usada pelo Windows Media Player para solicitar informações de sincronização de metadados aceleradas de dispositivos portáteis que não dão suporte a MTP. |
| [\_DEVICE2PC de \_ \_ viagem de \_ ida \_ e volta de metadados do WMP](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Estrutura usada pelo Windows Media Player para receber informações de sincronização de metadados aceleradas de dispositivos portáteis que não dão suporte a MTP. |



 

Para solicitar informações do dispositivo sobre metadados que foram alterados, o Windows Media Player 10 ou posterior chama o método IWMDMDevice3 do Windows Media Gerenciador de Dispositivos **::D eviceiocontrol**. Ao fazer essa chamada, o Player segue etapas específicas, da seguinte maneira:

-   O primeiro parâmetro, *dwIoControlCode*, contém a viagem de ida e volta de metadados do WMP do **IOCTL \_ \_ \_ \_** constante. Essa constante é definida em wmpdevices. h.
-   O segundo parâmetro, *lpInBuffer*, aponta para uma estrutura PC2DEVICE de viagem de ida e volta de **\_ \_ metadados \_ \_ \_ WMDM do WMP** .
-   O terceiro parâmetro, *nInBufferSize*, contém o tamanho do buffer de entrada.
-   O quarto parâmetro, *lpOutBuffer*, aponta para uma estrutura DEVICE2PC de viagem de ida e volta de **\_ \_ metadados \_ \_ \_ WMDM do WMP** . O dispositivo deve preencher essa estrutura com informações sobre as alterações.
-   O quinto parâmetro, *pnOutBufferSize*, recebe o tamanho do buffer de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




