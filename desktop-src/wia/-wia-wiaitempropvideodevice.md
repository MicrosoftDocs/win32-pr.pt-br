---
description: o driver de vídeo WIA (Windows Image Acquisition) padrão (wiavusd.dll) oferece suporte às seguintes propriedades para dispositivos de vídeo de streaming.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propriedade de dispositivo WIA de vídeo (Wiadef. h)
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

o driver de vídeo WIA (Windows Image Acquisition) padrão (wiavusd.dll) oferece suporte às seguintes propriedades para dispositivos de vídeo de streaming.

> [!Note]  
> o WIA não oferece suporte a dispositivos de vídeo no Windows Server 2003, Windows Vista ou posterior. para essas versões do Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

O prefixo "WIA \_ DPV \_ " indica uma propriedade de dispositivo para dispositivos de vídeo e é a Convenção de nomenclatura usada em C/C++. Para fins de script, essas constantes usam o prefixo "VideoDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.



| Constante/valor                                                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ última \_ imagem \_ realizada**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Essa propriedade é usada para notificar o driver WIA de que uma nova imagem foi adicionada. Os aplicativos devem definir o valor dessa propriedade como o nome do arquivo de imagem criado como resultado de uma chamada bem-sucedida para o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) . <br/> Tipo: VT \_ BSTR, acesso: leitura/gravação<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ \_ \_ Diretório de imagens DPV**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Essa propriedade é exposta pelo driver de modo de usuário de vídeo WIA padrão (wiavusd.dll). O valor dessa propriedade é o caminho completo do diretório em que o driver de vídeo WIA coloca imagens por padrão. Os aplicativos devem definir a propriedade [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) com esse valor. <br/> Tipo: VT \_ BSTR, acesso: somente leitura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ \_Caminho do \_ dispositivo \_ DPV DShow**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | o caminho completo do dispositivo de DirectShow. <br/> Tipo: VT \_ BSTR, acesso: somente leitura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ FileDeviceMountPoint \_ do \_ ponto de montagem DPF**</dt> <dt></dt> </dl>                              | Não implementado. <br/> Tipo: **VT \_ i4**, acesso: somente leitura, valores válidos: [WIA \_ prop \_ None](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
