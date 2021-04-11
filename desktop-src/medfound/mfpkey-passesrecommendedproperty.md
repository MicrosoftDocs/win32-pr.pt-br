---
description: Especifica o número máximo de passagens aceitas pelo codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Propriedade MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165382"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="a2926-103">\_Propriedade MFPKEY PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="a2926-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="a2926-104">Especifica o número máximo de passagens aceitas pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="a2926-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="a2926-105">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a2926-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a2926-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a2926-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="a2926-107">g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses</span><span class="sxs-lookup"><span data-stu-id="a2926-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="a2926-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="a2926-108">Data Type</span></span>

<span data-ttu-id="a2926-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="a2926-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="a2926-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2926-110">Remarks</span></span>

<span data-ttu-id="a2926-111">Você pode obter o valor dessa propriedade chamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="a2926-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="a2926-112">Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado usando a propriedade [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a2926-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2926-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2926-113">Requirements</span></span>



| <span data-ttu-id="a2926-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2926-114">Requirement</span></span> | <span data-ttu-id="a2926-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a2926-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2926-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2926-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2926-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2926-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2926-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2926-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2926-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2926-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2926-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2926-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2926-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2926-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2926-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2926-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2926-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2926-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




