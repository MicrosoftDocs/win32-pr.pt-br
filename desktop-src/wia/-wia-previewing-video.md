---
description: A interface IWiaVideo permite que um aplicativo exiba vídeo e Capture ainda imagens dele.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Visualizando vídeo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501781"
---
# <a name="previewing-video-wia"></a>Visualizando vídeo (WIA)

A interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) permite que um aplicativo exiba vídeo e Capture ainda imagens dele. Execute as etapas a seguir para selecionar o dispositivo de vídeo de streaming e exibir um fluxo de vídeo em uma janela.

-   Chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar um ponteiro para a interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) .
-   Use o método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) da interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) para obter um ponteiro para a interface [**de \_ \_ informações do dev IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Para obter instruções sobre como enumerar dispositivos, consulte Enumerando dispositivos do sistema.
-   Use a interface de [**\_ \_ informações de desenvolvimento do IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obter um ponteiro de interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo de aquisição de imagem do Windows (WIA) encontrado.
-   Use a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obter a propriedade DeviceID do dispositivo desejado. Um dispositivo de vídeo de streaming tem o sinalizador StiDeviceTypeStreamingVideo do \_ conjunto de propriedades do tipo de dev DIP WIA \_ \_ .
-   Use a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obter o valor da Propriedade do \_ diretório de imagens DPV do WIA \_ \_ .
-   Chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar um ponteiro para a interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .
-   Defina a propriedade [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) como o valor recebido do valor da Propriedade do diretório de \_ imagens DPV do WIA \_ \_ .
-   Chame [**IWiaVideo:: CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) na interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , passando a ID do dispositivo do dispositivo de imagem de streaming e o identificador da janela na qual o vídeo deve ser exibido.

> [!Note]  
> O WIA não oferece suporte a dispositivos de vídeo no Windows Server 2003, Windows Vista ou posterior. Para essas versões do Windows, use o [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

 

 
