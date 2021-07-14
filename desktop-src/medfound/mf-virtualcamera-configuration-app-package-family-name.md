---
description: Especifica o nome da família de pacotes de aplicativos para um aplicativo de configuração de câmera virtual.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691839"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="b6685-103">Atributo MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME</span><span class="sxs-lookup"><span data-stu-id="b6685-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="b6685-104">Especifica o nome da família de pacotes de aplicativos para um aplicativo de configuração de câmera virtual.</span><span class="sxs-lookup"><span data-stu-id="b6685-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="b6685-105">Quando fornecido, o pipeline associará o aplicativo de configuração à câmera virtual e fornecerá um ponto de lançamento dentro da página Configurações Câmera.</span><span class="sxs-lookup"><span data-stu-id="b6685-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6685-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b6685-106">Data type</span></span>

[<span data-ttu-id="b6685-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="b6685-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="b6685-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6685-108">Remarks</span></span>

<span data-ttu-id="b6685-109">Esse atributo pode ser exposto pela fonte de mídia personalizada da câmera virtual do armazenamento de atributos de origem de mídia [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span><span class="sxs-lookup"><span data-stu-id="b6685-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="b6685-110">Se o aplicativo de configuração ainda não estiver instalado no computador, o aplicativo Store será lançado e navegará até a página do aplicativo especificada pelo nome da família de pacotes.</span><span class="sxs-lookup"><span data-stu-id="b6685-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="b6685-111">Caso contrário, o aplicativo instalado será lançado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b6685-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="b6685-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6685-112">Requirements</span></span>



| <span data-ttu-id="b6685-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6685-113">Requirement</span></span> | <span data-ttu-id="b6685-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b6685-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6685-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6685-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6685-116">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="b6685-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="b6685-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6685-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6685-118">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="b6685-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="b6685-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6685-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6685-120"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="b6685-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6685-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b6685-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6685-122">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="b6685-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6685-123">**IMFAttributes::GetString**</span><span class="sxs-lookup"><span data-stu-id="b6685-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="b6685-124">**IMFAttributes::SetString**</span><span class="sxs-lookup"><span data-stu-id="b6685-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




