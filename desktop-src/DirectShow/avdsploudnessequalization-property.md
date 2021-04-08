---
description: Habilita ou desabilita a equalização de intensidade em um decodificador de áudio ou em um processador de sinais digitais (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propriedade AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920050"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="aa597-103">Propriedade AVDSPLoudnessEqualization</span><span class="sxs-lookup"><span data-stu-id="aa597-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="aa597-104">Habilita ou desabilita a equalização de intensidade em um decodificador de áudio ou em um processador de sinais digitais (DSP).</span><span class="sxs-lookup"><span data-stu-id="aa597-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="aa597-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa597-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa597-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aa597-106">Data type</span></span>

<span data-ttu-id="aa597-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aa597-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aa597-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="aa597-108">Property GUID</span></span>

<span data-ttu-id="aa597-109">**CODECAPI \_ AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="aa597-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="aa597-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aa597-110">Property value</span></span>

<span data-ttu-id="aa597-111">O valor dessa propriedade é um membro da enumeração [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .</span><span class="sxs-lookup"><span data-stu-id="aa597-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa597-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa597-112">Remarks</span></span>

<span data-ttu-id="aa597-113">A equalização de intensidade é um processo de DSP que mantém um nível de volume consistente quando o fluxo de áudio é alterado.</span><span class="sxs-lookup"><span data-stu-id="aa597-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa597-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa597-114">Requirements</span></span>



| <span data-ttu-id="aa597-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa597-115">Requirement</span></span> | <span data-ttu-id="aa597-116">Valor</span><span class="sxs-lookup"><span data-stu-id="aa597-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa597-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa597-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa597-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aa597-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aa597-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa597-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa597-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aa597-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aa597-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa597-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa597-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa597-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa597-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa597-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa597-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="aa597-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aa597-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aa597-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




