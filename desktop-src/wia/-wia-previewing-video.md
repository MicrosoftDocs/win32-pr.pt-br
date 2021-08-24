---
description: A interface IWiaVideo permite que um aplicativo veja vídeo e capture imagens ainda dele.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Visualizando vídeo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca270adf4e6461beac409315c782101744e8afeb72c33f07aa7bbc999e24751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813716"
---
# <a name="previewing-video-wia"></a>Visualizando vídeo (WIA)

A interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) permite que um aplicativo veja vídeo e capture imagens ainda dele. Execute as etapas a seguir para selecionar o dispositivo de vídeo de streaming e exibir um fluxo de vídeo em uma janela.

-   Chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar um ponteiro para a interface [**IWiaDevMgr.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)
-   Use o método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) da interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) para obter um ponteiro para a interface [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Para obter instruções sobre como enumerar dispositivos, consulte Enumerando dispositivos do sistema.
-   Use a interface [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obter um ponteiro de interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo WIA (Aquisição de Imagem Windows) encontrado.
-   Use a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obter a propriedade DeviceID do dispositivo desejado. Um dispositivo de vídeo de streaming tem o sinalizador DeviceTypeStreamingVideo do conjunto de propriedades WIA \_ DIP \_ DEV \_ TYPE.
-   Use a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obter o valor da propriedade \_ WIA DPV \_ IMAGES \_ DIRECTORY.
-   Chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar um ponteiro para a interface [**IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)
-   De definir a propriedade [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) como o valor recebido do valor da propriedade WIA \_ DPV \_ IMAGES \_ DIRECTORY.
-   Chame [**IWiaVideo::CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) na interface [**IWiaVideo,**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) passando a ID do dispositivo de imagem de streaming e a alça da janela na qual o vídeo será exibido.

> [!Note]  
> O WIA não dá suporte a dispositivos de vídeo Windows Server 2003, Windows Vista ou posterior. Para essas versões do Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

 

 
