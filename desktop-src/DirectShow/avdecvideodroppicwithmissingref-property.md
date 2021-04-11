---
description: Especifica se o decodificador cai intra frames com quadros de referência ausentes.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propriedade AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163761"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="70c21-103">Propriedade AVDecVideoDropPicWithMissingRef</span><span class="sxs-lookup"><span data-stu-id="70c21-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="70c21-104">Especifica se o decodificador cai intra frames com quadros de referência ausentes.</span><span class="sxs-lookup"><span data-stu-id="70c21-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="70c21-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="70c21-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="70c21-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="70c21-106">Data type</span></span>

<span data-ttu-id="70c21-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="70c21-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="70c21-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="70c21-108">Property GUID</span></span>

<span data-ttu-id="70c21-109">**CODECAPI \_ AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="70c21-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="70c21-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="70c21-110">Remarks</span></span>

<span data-ttu-id="70c21-111">Se o fragmentado estiver corrompido, um quadro poderá ter quadros de referência ausentes.</span><span class="sxs-lookup"><span data-stu-id="70c21-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="70c21-112">Se o valor dessa propriedade for **Variant \_ true**, o decodificador descartará o quadro.</span><span class="sxs-lookup"><span data-stu-id="70c21-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="70c21-113">Se o valor for **Variant \_ false**, o decodificador tentará decodificar o quadro, usando um ou mais quadros próximos como quadros de referência.</span><span class="sxs-lookup"><span data-stu-id="70c21-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="70c21-114">O quadro decodificado resultante terá artefatos de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="70c21-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c21-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c21-115">Requirements</span></span>



| <span data-ttu-id="70c21-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c21-116">Requirement</span></span> | <span data-ttu-id="70c21-117">Valor</span><span class="sxs-lookup"><span data-stu-id="70c21-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70c21-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70c21-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="70c21-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="70c21-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70c21-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="70c21-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="70c21-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70c21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c21-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c21-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c21-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="70c21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c21-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="70c21-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="70c21-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="70c21-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




