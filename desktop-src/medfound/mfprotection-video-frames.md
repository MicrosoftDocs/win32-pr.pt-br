---
description: Especifica se um aplicativo tem permissão para acessar quadros de vídeo descompactados.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Atributo MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763947"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="9458f-103">Atributo de quadros de \_ vídeo MFPROTECTION \_</span><span class="sxs-lookup"><span data-stu-id="9458f-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="9458f-104">Especifica se um aplicativo tem permissão para acessar quadros de vídeo descompactados.</span><span class="sxs-lookup"><span data-stu-id="9458f-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="9458f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9458f-105">Data type</span></span>

<span data-ttu-id="9458f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9458f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9458f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9458f-107">Remarks</span></span>

<span data-ttu-id="9458f-108">Um valor de 0 indica que o aplicativo tem permissão para acessar os quadros.</span><span class="sxs-lookup"><span data-stu-id="9458f-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="9458f-109">Isso pode ser determinado como resultado de um contrato privado entre o aplicativo e o sistema de proteção de conteúdo específico em uso.</span><span class="sxs-lookup"><span data-stu-id="9458f-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="9458f-110">Um valor de 1 indica que o aplicativo tem permissão para acessar quadros se um certificado de aplicativo válido for fornecido pelo aplicativo (consulte [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="9458f-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="9458f-111">Um valor de 0xFFFFFFFF, que é o valor padrão, indica que nenhum aplicativo tem permissão de acesso a quadros não compactados.</span><span class="sxs-lookup"><span data-stu-id="9458f-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="9458f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9458f-112">Requirements</span></span>



| <span data-ttu-id="9458f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9458f-113">Requirement</span></span> | <span data-ttu-id="9458f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9458f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9458f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9458f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9458f-116">\[Somente aplicativos UWP do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9458f-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9458f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9458f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9458f-118">Somente aplicativos UWP do Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9458f-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9458f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9458f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9458f-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9458f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9458f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9458f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9458f-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9458f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9458f-123">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="9458f-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




