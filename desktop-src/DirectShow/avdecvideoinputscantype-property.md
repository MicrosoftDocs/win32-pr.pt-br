---
description: Especifica como o fluxo de vídeo decodificado é entrelaçado.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propriedade AVDecVideoInputScanType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825897"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="952d2-103">Propriedade AVDecVideoInputScanType</span><span class="sxs-lookup"><span data-stu-id="952d2-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="952d2-104">Especifica como o fluxo de vídeo decodificado é entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="952d2-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="952d2-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="952d2-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="952d2-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="952d2-106">Data type</span></span>

<span data-ttu-id="952d2-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="952d2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="952d2-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="952d2-108">Property GUID</span></span>

<span data-ttu-id="952d2-109">**CODECAPI \_ AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="952d2-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="952d2-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="952d2-110">Property value</span></span>

<span data-ttu-id="952d2-111">O valor dessa propriedade é um membro da enumeração [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .</span><span class="sxs-lookup"><span data-stu-id="952d2-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="952d2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="952d2-112">Remarks</span></span>

<span data-ttu-id="952d2-113">Os 16 bits superiores do valor contêm a largura e os 16 bits inferiores contêm a altura.</span><span class="sxs-lookup"><span data-stu-id="952d2-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="952d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="952d2-114">Requirements</span></span>



| <span data-ttu-id="952d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="952d2-115">Requirement</span></span> | <span data-ttu-id="952d2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="952d2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="952d2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="952d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="952d2-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="952d2-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="952d2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="952d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="952d2-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="952d2-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="952d2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="952d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="952d2-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="952d2-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="952d2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="952d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952d2-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="952d2-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="952d2-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="952d2-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

