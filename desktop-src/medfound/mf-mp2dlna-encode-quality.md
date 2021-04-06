---
description: Especifica a qualidade de codificação para o coletor de mídia do DLNA (digital telenetwork Alliance).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Atributo MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011102"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="f3ab6-103">\_Atributo de \_ qualidade de codificação MP2DLNA MF \_</span><span class="sxs-lookup"><span data-stu-id="f3ab6-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="f3ab6-104">Especifica a qualidade de codificação para o coletor de mídia do DLNA (digital telenetwork Alliance).</span><span class="sxs-lookup"><span data-stu-id="f3ab6-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3ab6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f3ab6-105">Data type</span></span>

<span data-ttu-id="f3ab6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3ab6-106">**UINT32**</span></span>

<span data-ttu-id="f3ab6-107">Intervalo: 0 a 18</span><span class="sxs-lookup"><span data-stu-id="f3ab6-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="f3ab6-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="f3ab6-108">Get/set</span></span>

<span data-ttu-id="f3ab6-109">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f3ab6-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f3ab6-110">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f3ab6-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ab6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3ab6-111">Remarks</span></span>

<span data-ttu-id="f3ab6-112">Números mais altos indicam melhor qualidade de codificação.</span><span class="sxs-lookup"><span data-stu-id="f3ab6-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="f3ab6-113">Números mais baixos indicam codificação mais rápida, mas baixa qualidade de codificação.</span><span class="sxs-lookup"><span data-stu-id="f3ab6-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="f3ab6-114">O valor padrão é 9.</span><span class="sxs-lookup"><span data-stu-id="f3ab6-114">The default value is 9.</span></span>

<span data-ttu-id="f3ab6-115">Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="f3ab6-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="f3ab6-116">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="f3ab6-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ab6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ab6-117">Requirements</span></span>



| <span data-ttu-id="f3ab6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ab6-118">Requirement</span></span> | <span data-ttu-id="f3ab6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f3ab6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ab6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3ab6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ab6-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3ab6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f3ab6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3ab6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ab6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f3ab6-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f3ab6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3ab6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3ab6-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ab6-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ab6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3ab6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ab6-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3ab6-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




