---
description: Especifica o tipo de unidade contida em um IMFSample em uma \_ coleção de ForwardedDecodeUnits MFSampleExtension.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Enumeração de MF_CUSTOM_DECODE_UNIT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165030"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="385ea-103">\_Enumeração de \_ tipo de unidade de decodificação personalizada MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="385ea-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="385ea-104">Especifica o tipo de unidade contida em um [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) em uma coleção de [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .</span><span class="sxs-lookup"><span data-stu-id="385ea-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="385ea-105">Membros</span><span class="sxs-lookup"><span data-stu-id="385ea-105">Members</span></span>



| <span data-ttu-id="385ea-106">Membro</span><span class="sxs-lookup"><span data-stu-id="385ea-106">Member</span></span>                    | <span data-ttu-id="385ea-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="385ea-107">Description</span></span>                                                             | <span data-ttu-id="385ea-108">Valor</span><span class="sxs-lookup"><span data-stu-id="385ea-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="385ea-109">**\_nal de unidade de decodificação MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="385ea-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="385ea-110">O tipo de unidade é NALU (unidade de camada de abstração de rede).</span><span class="sxs-lookup"><span data-stu-id="385ea-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="385ea-111">0</span><span class="sxs-lookup"><span data-stu-id="385ea-111">0</span></span>     |
| <span data-ttu-id="385ea-112">**\_unidade de decodificação de MF \_ \_ sei**</span><span class="sxs-lookup"><span data-stu-id="385ea-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="385ea-113">O tipo de unidade é informações de aprimoramento complementar (SEI).</span><span class="sxs-lookup"><span data-stu-id="385ea-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="385ea-114">1</span><span class="sxs-lookup"><span data-stu-id="385ea-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="385ea-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="385ea-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="385ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="385ea-116">Requirements</span></span>



| <span data-ttu-id="385ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="385ea-117">Requirement</span></span> | <span data-ttu-id="385ea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="385ea-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="385ea-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="385ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="385ea-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="385ea-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="385ea-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="385ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="385ea-122">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="385ea-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="385ea-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="385ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="385ea-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="385ea-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




