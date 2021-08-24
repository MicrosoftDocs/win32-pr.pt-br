---
title: Windows Extensões Gerenciador de Dispositivos dispositivo de mídia para transferência de metadados
description: Windows Extensões Gerenciador de Dispositivos dispositivo de mídia para transferência de metadados
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player,extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, metadados
- Windows Media Player transferência de metadados acelerada
- Windows Media Player transferência acelerada de metadados
- metadados, extensões de dispositivo
- metadados, extensões
- extensões de dispositivo, transferência de metadados
- extensões, transferência de metadados
- transferência de metadados acelerada
- metadados, transferência acelerada
- extensões de dispositivo, transferência de metadados acelerada
- extensões, transferência acelerada de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9b37271fc9714bf3665dccf1475da1a5840c429d7df9136a50fe95789f7a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571627"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Extensões Gerenciador de Dispositivos dispositivo de mídia para transferência de metadados

Para habilitar a transferência acelerada de metadados, os fabricantes de dispositivos que não são compatíveis com MTP devem fazer o seguinte no código-fonte:

-   Defina **SUPORTE \_ AO DISPOSITIVO WMP \_ \_ WMDM.**
-   Inclua wmpdevices.h, que é instalado como parte do SDK do Windows Media Player.

Wmpdevices.h define as estruturas a seguir.



| Estrutura                                                                                 | Descrição                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Estrutura usada pelo Windows Media Player para solicitar informações de sincronização de metadados aceleradas de dispositivos portáteis que não são compatíveis com MTP. |
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Estrutura usada pelo Windows Media Player para receber informações de sincronização de metadados aceleradas de dispositivos portáteis que não são compatíveis com MTP. |



 

Para solicitar informações do dispositivo sobre metadados que foram alterados, o Windows Media Player 10 ou posterior chama o método Gerenciador de Dispositivos media **Windows IWMDMDevice3::D eviceIoControl.** Ao fazer essa chamada, o Player segue etapas específicas, da seguinte forma:

-   O primeiro parâmetro, *dwIoControlCode,* contém a constante **IOCTL \_ WMP \_ METADATA \_ ROUND \_ TRIP**. Essa constante é definida em wmpdevices.h.
-   O segundo parâmetro, *lpInBuffer,* aponta para uma estrutura **WMP \_ WMDM WMDM \_ ROUND TRIP \_ \_ \_ PC2DEVICE.**
-   O terceiro parâmetro, *nInBufferSize,* contém o tamanho do buffer de entrada.
-   O quarto parâmetro, *lpOutBuffer,* aponta para uma estrutura **WMP \_ WMDM WMDM \_ ROUND TRIP \_ \_ \_ DEVICE2PC.** O dispositivo deve preencher essa estrutura com informações sobre alterações.
-   O quinto parâmetro, *pnOutBufferSize,* recebe o tamanho do buffer de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados aceleradas**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




