---
description: Especifica se o coletor de mídia de rede de vida digital (DLNA) usa o serviço do Agendador de classes de multimídia (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Atributo MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011100"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="2fd21-103">MF \_ MP2DLNA \_ usar o \_ atributo MMCSS</span><span class="sxs-lookup"><span data-stu-id="2fd21-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="2fd21-104">Especifica se o coletor de mídia de rede de vida digital (DLNA) usa o serviço do Agendador de classes de multimídia (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="2fd21-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="2fd21-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2fd21-105">Data type</span></span>

<span data-ttu-id="2fd21-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2fd21-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="2fd21-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="2fd21-107">Get/set</span></span>

<span data-ttu-id="2fd21-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2fd21-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2fd21-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2fd21-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd21-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fd21-110">Remarks</span></span>

<span data-ttu-id="2fd21-111">Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2fd21-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="2fd21-112">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="2fd21-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="2fd21-113">Se esse atributo for **true**, o coletor de mídia DLNA se registrará com o MMCSS.</span><span class="sxs-lookup"><span data-stu-id="2fd21-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd21-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd21-114">Requirements</span></span>



| <span data-ttu-id="2fd21-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd21-115">Requirement</span></span> | <span data-ttu-id="2fd21-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2fd21-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd21-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fd21-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd21-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2fd21-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2fd21-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fd21-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd21-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2fd21-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2fd21-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fd21-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd21-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd21-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd21-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fd21-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd21-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2fd21-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




