---
description: Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Propriedade MFPKEY_DYN_VBR_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751508"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="0e040-103">\_Propriedade MFPKEY dyn \_ VBR \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="0e040-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="0e040-104">Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="0e040-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0e040-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0e040-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0e040-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="0e040-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0e040-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="0e040-107">Data Type</span></span>

<span data-ttu-id="0e040-108">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="0e040-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e040-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e040-109">Remarks</span></span>

<span data-ttu-id="0e040-110">Se as propriedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) estiverem definidas como **Variant \_ true**, o codificador usará a codificação de taxa de bits média controlável.</span><span class="sxs-lookup"><span data-stu-id="0e040-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="0e040-111">Nesse caso, o codificador se configura de acordo com o valor dessa propriedade e a propriedade [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0e040-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e040-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e040-112">Requirements</span></span>



| <span data-ttu-id="0e040-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e040-113">Requirement</span></span> | <span data-ttu-id="0e040-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0e040-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e040-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e040-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0e040-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e040-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e040-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e040-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0e040-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e040-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e040-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e040-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e040-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e040-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e040-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e040-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e040-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e040-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
