---
description: Quando um aplicativo se conecta a um dispositivo de hardware WIA (Aquisição de Imagem) do Windows, o WIA cria uma árvore de itens (uma árvore hierárquica de interfaces IWiaItem ou IWiaItem2) que representa o dispositivo e suas imagens, pastas e colchas de verificação.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Selecionando um dispositivo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d068dc2501419b5748f199114fab15d72dc5fecc6c7e6881f63b8e47114b7d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813647"
---
# <a name="selecting-a-device-wia"></a>Selecionando um dispositivo (WIA)

Quando um aplicativo se conecta a um dispositivo de hardware WIA (Aquisição de Imagem) do Windows, o WIA cria uma árvore de itens (uma árvore hierárquica de interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2)**](-wia-iwiaitem2.md) que representa o dispositivo e suas imagens, pastas e colchas de verificação. Um aplicativo pode selecionar e se conectar a um dispositivo sem entrada do usuário ou pode exibir uma caixa de diálogo que permite que um usuário selecione um dispositivo.

-   [Selecionando um dispositivo sem a interface do usuário](#selecting-a-device-without-the-ui)
-   [Selecionando um dispositivo com a interface do usuário](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Selecionando um dispositivo sem a interface do usuário

Execute as etapas a seguir para selecionar e conectar-se a um dispositivo de hardware WIA.

-   Chame [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar um ponteiro para a interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) [**ou IWiaDevMgr2.**](-wia-iwiadevmgr2.md)
-   Use o método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) da interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) para obter um ponteiro para a interface [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Para obter instruções sobre como enumerar dispositivos, consulte [Enumerando dispositivos do sistema](-wia-enumerating-system-devices.md).
-   Use a interface [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obter ponteiros de interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo WIA enumerado.
-   Use a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para inspecionar as propriedades de informações do dispositivo de cada dispositivo e salvar a propriedade ID deV dip do WIA do \_ \_ dispositivo \_ desejado.
-   Use a propriedade DeviceID com o método [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) na interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) para criar um objeto de dispositivo WIA. O método **IWiaDevMgr::CreateDevice** fornece ao aplicativo o ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz do dispositivo especificado.

Para ver um exemplo de como fazer isso em um aplicativo, consulte [Criando um](-wia-creating-a-device.md) dispositivo na seção do tutorial deste guia.

## <a name="selecting-a-device-with-the-ui"></a>Selecionando um dispositivo com a interface do usuário

Depois de recuperar um ponteiro para [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), um aplicativo pode permitir que um usuário selecione um dispositivo ignorando o restante das etapas acima e chamando [**IWiaDevMgr::SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg). O **IWiaDevMgr::SelectDeviceDlg** exibe uma caixa de diálogo na qual o usuário pode selecionar um dispositivo WIA.

É recomendável que os aplicativos disponibilizam a seleção de dispositivo e imagem por meio de um item de menu chamado **Do scanner** no menu **Arquivo.**

 

 
