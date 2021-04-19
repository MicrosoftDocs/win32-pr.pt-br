---
description: Especifica o tipo de filtro de ênfase que deve ser usado ao decodificar. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propriedade AVEncMPAEmphasisType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810954"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="c264e-104">Propriedade AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="c264e-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="c264e-105">Especifica o tipo de filtro de ênfase que deve ser usado ao decodificar.</span><span class="sxs-lookup"><span data-stu-id="c264e-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="c264e-106">Essa propriedade se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="c264e-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="c264e-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c264e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c264e-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c264e-108">Data type</span></span>

<span data-ttu-id="c264e-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c264e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c264e-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c264e-110">Property GUID</span></span>

<span data-ttu-id="c264e-111">**CODECAPI \_ AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="c264e-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="c264e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c264e-112">Property value</span></span>

<span data-ttu-id="c264e-113">O valor dessa propriedade é um membro da enumeração [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .</span><span class="sxs-lookup"><span data-stu-id="c264e-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="c264e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c264e-114">Remarks</span></span>

<span data-ttu-id="c264e-115">Essa propriedade define os bits de ênfase no cabeçalho do quadro.</span><span class="sxs-lookup"><span data-stu-id="c264e-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="c264e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c264e-116">Requirements</span></span>



| <span data-ttu-id="c264e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c264e-117">Requirement</span></span> | <span data-ttu-id="c264e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c264e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c264e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c264e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c264e-120">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c264e-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c264e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c264e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c264e-122">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c264e-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c264e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c264e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c264e-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c264e-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c264e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c264e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c264e-126">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="c264e-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c264e-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c264e-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

