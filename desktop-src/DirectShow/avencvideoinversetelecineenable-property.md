---
description: Especifica se o codificador executa o telecineon inverso.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propriedade AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087764"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="cfc2f-103">Propriedade AVEncVideoInverseTelecineEnable</span><span class="sxs-lookup"><span data-stu-id="cfc2f-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="cfc2f-104">Especifica se o codificador executa o telecineon inverso.</span><span class="sxs-lookup"><span data-stu-id="cfc2f-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="cfc2f-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cfc2f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfc2f-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cfc2f-106">Data type</span></span>

<span data-ttu-id="cfc2f-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="cfc2f-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cfc2f-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="cfc2f-108">Property GUID</span></span>

<span data-ttu-id="cfc2f-109">**CODECAPI \_ AVEncVideoInverseTelecineEnable**</span><span class="sxs-lookup"><span data-stu-id="cfc2f-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc2f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfc2f-110">Remarks</span></span>

<span data-ttu-id="cfc2f-111">Se o valor for **Variant \_ true**, o codificador executará o telecineon inverso.</span><span class="sxs-lookup"><span data-stu-id="cfc2f-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="cfc2f-112">Se o telecineon inverso não for necessário, defina essa propriedade como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cfc2f-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="cfc2f-113">Para executar o telecineon inverso fora do codificador, defina essa propriedade como **Variant \_ false** e defina a propriedade [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) como eAVEncVideoOutputScan \_ SameAsInput.</span><span class="sxs-lookup"><span data-stu-id="cfc2f-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc2f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfc2f-114">Requirements</span></span>



| <span data-ttu-id="cfc2f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc2f-115">Requirement</span></span> | <span data-ttu-id="cfc2f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cfc2f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc2f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfc2f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc2f-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfc2f-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cfc2f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfc2f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc2f-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfc2f-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cfc2f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfc2f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc2f-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc2f-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc2f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfc2f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc2f-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="cfc2f-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cfc2f-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cfc2f-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




