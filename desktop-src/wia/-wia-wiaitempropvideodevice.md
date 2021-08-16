---
description: O driver de Windows wia (aquisição de imagem) padrão (wiavusd.dll) dá suporte às propriedades a seguir para streaming de dispositivos de vídeo.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propriedade de dispositivo WIA de vídeo (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 9652ac72d6e73a9c44d2f4b299823dad9cc566bb1c7c0129af497ea213a6e5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207364"
---
# <a name="video-wia-device-property-constants"></a>Constantes de propriedade de dispositivo WIA de vídeo

O driver de Windows wia (aquisição de imagem) padrão (wiavusd.dll) dá suporte às propriedades a seguir para streaming de dispositivos de vídeo.

> [!Note]  
> O WIA não dá suporte a dispositivos de vídeo Windows Server 2003, Windows Vista ou posterior. Para essas versões do Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

O prefixo "WIA DPV" indica uma propriedade de dispositivo para dispositivos de vídeo e é a convenção de nomen entre \_ \_ C/C++. Para fins de script, essas constantes usam o prefixo "VideoDevice" e fazem parte do tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) O nome do membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome constante C/C++ na lista a seguir.



| Constante/valor                                                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ LAST \_ PICTURE \_ TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Essa propriedade é usada para notificar o driver WIA de que uma nova imagem foi adicionada. Os aplicativos devem definir o valor dessa propriedade como o nome do arquivo de imagem criado como resultado de uma chamada bem-sucedida para o método [**IWiaVideo::TakePicture.**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) <br/> Tipo: VT \_ BSTR, Acesso: Leitura/Gravação<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ DPV \_ IMAGES \_ DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Essa propriedade é exposta pelo driver de modo de usuário de vídeo wi-fi padrão (wiavusd.dll). O valor dessa propriedade é o caminho completo do diretório em que o driver de vídeo WIA coloca imagens por padrão. Os aplicativos devem definir [**a propriedade IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) para esse valor. <br/> Tipo: VT \_ BSTR, Acesso: Somente Leitura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ DPV \_ DSHOW \_ DEVICE \_ PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | O caminho completo do DirectShow dispositivo. <br/> Tipo: VT \_ BSTR, Acesso: Somente Leitura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ Arquivo \_ DE PONTO \_ DE MONTAGEM**</dt> do DPFDeviceMountPoint <dt></dt> </dl>                              | Não implementado. <br/> Tipo: **VT \_ I4**, Acesso: Somente Leitura, Valores válidos: [WIA \_ PROP \_ NONE](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
