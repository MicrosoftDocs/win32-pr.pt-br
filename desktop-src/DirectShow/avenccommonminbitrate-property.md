---
description: Especifica a taxa de bits mínima, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Propriedade AVEncCommonMinBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813000"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="56026-104">Propriedade AVEncCommonMinBitRate</span><span class="sxs-lookup"><span data-stu-id="56026-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="56026-105">Especifica a taxa de bits mínima, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="56026-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="56026-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="56026-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="56026-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="56026-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="56026-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="56026-108">Data type</span></span>

<span data-ttu-id="56026-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="56026-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="56026-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="56026-110">Property GUID</span></span>

<span data-ttu-id="56026-111">**CODECAPI \_ AVEncCommonMinBitRate**</span><span class="sxs-lookup"><span data-stu-id="56026-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="56026-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="56026-112">Property value</span></span>

<span data-ttu-id="56026-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="56026-113">This property has a linear range of values.</span></span> <span data-ttu-id="56026-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="56026-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="56026-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="56026-115">Remarks</span></span>

<span data-ttu-id="56026-116">O codificador impõe a taxa de bits mínima aumentando a qualidade de codificação conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="56026-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="56026-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56026-117">Requirements</span></span>



| <span data-ttu-id="56026-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56026-118">Requirement</span></span> | <span data-ttu-id="56026-119">Valor</span><span class="sxs-lookup"><span data-stu-id="56026-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56026-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56026-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56026-121">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="56026-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="56026-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56026-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56026-123">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="56026-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="56026-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56026-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="56026-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56026-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56026-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="56026-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56026-127">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="56026-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="56026-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="56026-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




