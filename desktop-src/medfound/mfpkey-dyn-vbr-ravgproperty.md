---
description: Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Propriedade MFPKEY_DYN_VBR_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921401"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="41f9a-103">\_Propriedade MFPKEY dyn \_ VBR \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="41f9a-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="41f9a-104">Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="41f9a-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="41f9a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="41f9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="41f9a-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="41f9a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="41f9a-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="41f9a-107">Data Type</span></span>

<span data-ttu-id="41f9a-108">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="41f9a-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="41f9a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="41f9a-109">Remarks</span></span>

<span data-ttu-id="41f9a-110">Se as propriedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) estiverem definidas como **Variant \_ true**, o codificador usará a codificação de taxa de bits média controlável.</span><span class="sxs-lookup"><span data-stu-id="41f9a-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="41f9a-111">Nesse caso, o codificador se configura de acordo com o valor dessa propriedade e a propriedade [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="41f9a-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f9a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f9a-112">Requirements</span></span>



| <span data-ttu-id="41f9a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f9a-113">Requirement</span></span> | <span data-ttu-id="41f9a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="41f9a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41f9a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="41f9a-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41f9a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="41f9a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="41f9a-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41f9a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41f9a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41f9a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f9a-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f9a-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f9a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="41f9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f9a-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41f9a-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
