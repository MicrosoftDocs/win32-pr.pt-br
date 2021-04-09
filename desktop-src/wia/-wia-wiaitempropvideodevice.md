---
description: O driver padrão de vídeo WIA (Windows Image Acquisition) (wiavusd.dll) oferece suporte às seguintes propriedades para dispositivos de vídeo de streaming.
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
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090484"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="a4efb-103">Constantes de propriedade de dispositivo WIA de vídeo</span><span class="sxs-lookup"><span data-stu-id="a4efb-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="a4efb-104">O driver padrão de vídeo WIA (Windows Image Acquisition) (wiavusd.dll) oferece suporte às seguintes propriedades para dispositivos de vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="a4efb-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="a4efb-105">O WIA não oferece suporte a dispositivos de vídeo no Windows Server 2003, Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a4efb-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="a4efb-106">Para essas versões do Windows, use o [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4efb-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="a4efb-107">O prefixo "WIA \_ DPV \_ " indica uma propriedade de dispositivo para dispositivos de vídeo e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="a4efb-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="a4efb-108">Para fins de script, essas constantes usam o prefixo "VideoDevice" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="a4efb-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="a4efb-109">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4efb-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="a4efb-110">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="a4efb-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="a4efb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4efb-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="a4efb-112"><dt>**WIA \_ DPV \_ última \_ imagem \_ realizada**</dt> <dt>VideoDeviceLastPictureTaken</dt></span><span class="sxs-lookup"><span data-stu-id="a4efb-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="a4efb-113">Essa propriedade é usada para notificar o driver WIA de que uma nova imagem foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="a4efb-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="a4efb-114">Os aplicativos devem definir o valor dessa propriedade como o nome do arquivo de imagem criado como resultado de uma chamada bem-sucedida para o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) .</span><span class="sxs-lookup"><span data-stu-id="a4efb-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="a4efb-115">Tipo: VT \_ BSTR, acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a4efb-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="a4efb-116"><dt>**WIA \_ \_ \_ Diretório de imagens DPV**</dt> <dt>VideoDeviceImagesDirectory</dt></span><span class="sxs-lookup"><span data-stu-id="a4efb-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="a4efb-117">Essa propriedade é exposta pelo driver de modo de usuário de vídeo WIA padrão (wiavusd.dll).</span><span class="sxs-lookup"><span data-stu-id="a4efb-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="a4efb-118">O valor dessa propriedade é o caminho completo do diretório em que o driver de vídeo WIA coloca imagens por padrão.</span><span class="sxs-lookup"><span data-stu-id="a4efb-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="a4efb-119">Os aplicativos devem definir a propriedade [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) com esse valor.</span><span class="sxs-lookup"><span data-stu-id="a4efb-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="a4efb-120">Tipo: VT \_ BSTR, acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4efb-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="a4efb-121"><dt>**WIA \_ \_Caminho do \_ dispositivo \_ DPV DShow**</dt> <dt>VideoDeviceDShowDevicePath</dt></span><span class="sxs-lookup"><span data-stu-id="a4efb-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="a4efb-122">O caminho completo do dispositivo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a4efb-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="a4efb-123">Tipo: VT \_ BSTR, acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4efb-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="a4efb-124"><dt>**WIA \_ FileDeviceMountPoint \_ do \_ ponto de montagem DPF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a4efb-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="a4efb-125">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a4efb-125">Not implemented.</span></span> <br/> <span data-ttu-id="a4efb-126">Tipo: **VT \_ i4**, acesso: somente leitura, valores válidos: [WIA \_ prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="a4efb-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="a4efb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4efb-127">Requirements</span></span>



| <span data-ttu-id="a4efb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4efb-128">Requirement</span></span> | <span data-ttu-id="a4efb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a4efb-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4efb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4efb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a4efb-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4efb-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a4efb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4efb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a4efb-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4efb-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a4efb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4efb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4efb-135"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4efb-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
