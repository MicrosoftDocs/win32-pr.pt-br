---
description: Especifica se o chamador vai alocar as texturas usadas para saída.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Atributo MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502103"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="2c7a0-103">O \_ chamador XVP do MF \_ aloca o atributo de \_ \_ saída</span><span class="sxs-lookup"><span data-stu-id="2c7a0-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="2c7a0-104">Especifica se o chamador vai alocar as texturas usadas para saída.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c7a0-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2c7a0-105">Data type</span></span>

<span data-ttu-id="2c7a0-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2c7a0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c7a0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c7a0-107">Remarks</span></span>

<span data-ttu-id="2c7a0-108">Se esse atributo for **true**, o processador de vídeo esperará que as texturas de saída sejam alocadas pelo chamador, mesmo quando estiverem operando no modo DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="2c7a0-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="2c7a0-109">Se esse atributo for **false**, o processador de vídeo alocará as texturas de saída ao operar no modo de DXVA e falhará se as texturas de saída fornecidas pelo chamador forem fornecidas.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="2c7a0-110">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="2c7a0-110">To set this attribute:</span></span>

1.  <span data-ttu-id="2c7a0-111">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="2c7a0-112">Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2c7a0-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="2c7a0-113">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7a0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c7a0-114">Requirements</span></span>



| <span data-ttu-id="2c7a0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c7a0-115">Requirement</span></span> | <span data-ttu-id="2c7a0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2c7a0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7a0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c7a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7a0-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c7a0-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2c7a0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c7a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7a0-120">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2c7a0-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2c7a0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c7a0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c7a0-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c7a0-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c7a0-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="2c7a0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c7a0-124"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c7a0-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c7a0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c7a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7a0-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c7a0-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




