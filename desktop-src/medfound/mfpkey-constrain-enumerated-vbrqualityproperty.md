---
description: Especifica se os modos enumerados pelo codificador são Limeted àqueles que atendem a um requisito de qualidade fornecido pelo \_ VBRQUALITY desejado do MFPKEY \_ .
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Propriedade MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761003"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="5c943-103">MFPKEY \_ restringir a \_ \_ Propriedade VBRQUALITY enumerada</span><span class="sxs-lookup"><span data-stu-id="5c943-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="5c943-104">Especifica se os modos enumerados pelo codificador são Limeted àqueles que atendem a um requisito de qualidade fornecido pelo [**\_ \_ VBRQUALITY desejado do MFPKEY**](mfpkey-desired-vbrqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="5c943-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5c943-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5c943-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5c943-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5c943-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5c943-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5c943-107">Data Type</span></span>

<span data-ttu-id="5c943-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="5c943-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="5c943-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="5c943-109">Default Value</span></span>

<span data-ttu-id="5c943-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="5c943-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="5c943-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c943-111">Remarks</span></span>

<span data-ttu-id="5c943-112">Para enumerar modos de VBR que atendam a um determinado requisito de qualidade, defina as propriedades do codificador a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c943-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="5c943-113">Defina [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="5c943-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="5c943-114">Defina **MFPKEY \_ restringir \_ enumerated \_ VBRQUALITY** para **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="5c943-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="5c943-115">Defina [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) para a qualidade desejada.</span><span class="sxs-lookup"><span data-stu-id="5c943-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="5c943-116">Para modos sem perdas, defina a qualidade desejada como 100.</span><span class="sxs-lookup"><span data-stu-id="5c943-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c943-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c943-117">Requirements</span></span>



| <span data-ttu-id="5c943-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c943-118">Requirement</span></span> | <span data-ttu-id="5c943-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5c943-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c943-120">Cliente</span><span class="sxs-lookup"><span data-stu-id="5c943-120">Client</span></span><br/> | <span data-ttu-id="5c943-121">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c943-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="5c943-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c943-122">Header</span></span><br/> | <dl> <span data-ttu-id="5c943-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c943-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c943-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c943-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c943-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c943-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
