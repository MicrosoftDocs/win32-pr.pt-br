---
description: Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4 ou usa um downmix não padrão.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propriedade AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757901"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="84e5d-103">Propriedade AVDecAACDownmixMode</span><span class="sxs-lookup"><span data-stu-id="84e5d-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="84e5d-104">Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4 ou usa um downmix não padrão.</span><span class="sxs-lookup"><span data-stu-id="84e5d-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="84e5d-105">Um exemplo de um downmix não padrão é o definido por ARIB do documento STD-B21 versão 4,4.</span><span class="sxs-lookup"><span data-stu-id="84e5d-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="84e5d-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="84e5d-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="84e5d-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="84e5d-107">Data type</span></span>

<span data-ttu-id="84e5d-108">**UINT32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="84e5d-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="84e5d-109">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="84e5d-109">Property GUID</span></span>

<span data-ttu-id="84e5d-110">**CODECAPI \_ AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="84e5d-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="84e5d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="84e5d-111">Property value</span></span>

<span data-ttu-id="84e5d-112">O valor dessa propriedade é um membro da enumeração [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="84e5d-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e5d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84e5d-113">Requirements</span></span>



| <span data-ttu-id="84e5d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84e5d-114">Requirement</span></span> | <span data-ttu-id="84e5d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="84e5d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84e5d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84e5d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84e5d-117">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84e5d-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="84e5d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84e5d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84e5d-119">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84e5d-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="84e5d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84e5d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e5d-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e5d-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e5d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="84e5d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e5d-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="84e5d-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="84e5d-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="84e5d-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

