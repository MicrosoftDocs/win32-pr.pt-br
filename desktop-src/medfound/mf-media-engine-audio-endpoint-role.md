---
description: Especifica a função de dispositivo para o fluxo de áudio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105788987"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a><span data-ttu-id="1f084-103">\_Atributo de \_ função de \_ ponto de extremidade de áudio do mecanismo \_ de mídia \_ MF</span><span class="sxs-lookup"><span data-stu-id="1f084-103">MF\_MEDIA\_ENGINE\_AUDIO\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="1f084-104">Especifica a função de dispositivo para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1f084-104">Specifies the device role for the audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f084-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1f084-105">Data type</span></span>

<span data-ttu-id="1f084-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1f084-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1f084-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f084-107">Remarks</span></span>

<span data-ttu-id="1f084-108">O valor desse atributo é um membro da enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="1f084-108">The value of this attribute is a member of the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>

<span data-ttu-id="1f084-109">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1f084-109">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="1f084-110">O atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="1f084-110">The attribute is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f084-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f084-111">Requirements</span></span>



| <span data-ttu-id="1f084-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f084-112">Requirement</span></span> | <span data-ttu-id="1f084-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1f084-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f084-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f084-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f084-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1f084-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="1f084-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f084-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f084-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1f084-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1f084-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f084-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f084-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f084-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f084-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f084-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f084-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f084-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
