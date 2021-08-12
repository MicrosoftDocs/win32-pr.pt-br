---
title: Habilitando PnP para dispositivos
description: Habilitando PnP para dispositivos
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Mídia Gerenciador de Dispositivos, dispositivos PnP
- Dispositivos Gerenciador de Dispositivos, PnP
- Guia de programação, dispositivos PnP
- provedores de serviço, dispositivos PnP
- criando provedores de serviços, dispositivos PnP
- Dispositivos PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e574aa0d5462c2fcbb0592e9d3faaf927cd7e5213e6eec3d8e7f016eabfb7abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584994"
---
# <a name="enabling-pnp-for-devices"></a>Habilitando PnP para dispositivos

Windows A mídia Gerenciador de Dispositivos monitora as notificações de chegada e remoção de dispositivos que anunciam uma interface de dispositivo de player de áudio portátil. na chegada desse dispositivo, Windows mídia Gerenciador de Dispositivos consulta um parâmetro de dispositivo chamado *WMDMSPCLSID* para a ID de classe do provedor de serviços responsável por este dispositivo. Windows Mídia Gerenciador de Dispositivos chama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) neste provedor de serviços para criar um objeto de dispositivo, que é exposto ao aplicativo como um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

Um provedor de serviços pode lidar com dispositivos PnP ou dispositivos não-PnP; Ele não pode lidar com ambos os tipos.

para que um dispositivo funcione com o mecanismo anterior (e, portanto, habilite as notificações de chegada e remoção para o dispositivo em Windows mídia Gerenciador de Dispositivos aplicativos), os seguintes requisitos devem ser atendidos:

-   o driver de dispositivo deste dispositivo deve anunciar o Windows mídia Gerenciador de Dispositivos interface de dispositivo do Player de áudio portátil. O GUID dessa interface de dispositivo é definido como:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Um dispositivo não deve anunciar essa interface se o dispositivo anunciar a interface de volume (definida como VolumeClassGuid ou \_ volume DEVINTERFACE GUID \_ em winioctl. h). se o dispositivo anunciar a Interface do Volume, ele já estará habilitado para PnP em Windows mídia Gerenciador de Dispositivos.

     

    -E/OU-

    uma nova subchave do registro para o provedor de serviços deve ser criada dentro da subchave HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media Gerenciador de Dispositivos \\ KnownDevices. Essa chave deve ter o nome do seu provedor de serviços e deve ter as duas entradas de valor do reg sz a seguir \_ :

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   O dispositivo deve ter um parâmetro de dispositivo chamado WMDMSPCLSID. O valor desse parâmetro deve ser definido como o CLSID do provedor de serviços em um formulário de cadeia de caracteres. Para obter mais informações sobre os parâmetros do dispositivo, consulte [parâmetros do dispositivo](device-parameters.md).

    > [!Note]  
    > O valor do parâmetro deve ser o CLSID, não o ProgID do provedor de serviços.

     

-   O provedor de serviços para este dispositivo deve implementar a interface IMDServiceProvider2.
-   a chave do provedor de serviços em HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media Gerenciador de Dispositivos \\ Plugins \\ SP \\ de nome de arquivo deve conter o seguinte valor DWORD
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 




