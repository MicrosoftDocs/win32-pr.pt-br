---
description: Especifica o nível de qualidade desejado para codificação de taxa de bits variável (VBR) baseada em qualidade (1-pass) de fluxos de áudio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Propriedade MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751538"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="fabdb-103">MFPKEY \_ desired \_ VBRQUALITY Property</span><span class="sxs-lookup"><span data-stu-id="fabdb-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="fabdb-104">Especifica o nível de qualidade desejado para codificação de taxa de bits variável (VBR) baseada em qualidade (1-pass) de fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="fabdb-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fabdb-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fabdb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fabdb-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="fabdb-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="fabdb-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="fabdb-107">Data Type</span></span>

<span data-ttu-id="fabdb-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="fabdb-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="fabdb-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="fabdb-109">Default Value</span></span>

<span data-ttu-id="fabdb-110">0</span><span class="sxs-lookup"><span data-stu-id="fabdb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="fabdb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fabdb-111">Remarks</span></span>

<span data-ttu-id="fabdb-112">Esse valor pode ser de 0 a 100, onde 100 é a qualidade máxima.</span><span class="sxs-lookup"><span data-stu-id="fabdb-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="fabdb-113">Um valor de 0 indica que o método de codificação VBR com base em qualidade não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fabdb-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="fabdb-114">Para enumerar modos de VBR que atendam a um determinado requisito de qualidade, defina as propriedades do codificador a seguir.</span><span class="sxs-lookup"><span data-stu-id="fabdb-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="fabdb-115">Defina [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="fabdb-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="fabdb-116">Defina [**MFPKEY \_ restringir \_ enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) para **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="fabdb-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="fabdb-117">Defina **MFPKEY \_ desired \_ VBRQUALITY** para a qualidade desejada.</span><span class="sxs-lookup"><span data-stu-id="fabdb-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="fabdb-118">Para modos sem perdas, defina a qualidade desejada como 100.</span><span class="sxs-lookup"><span data-stu-id="fabdb-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="fabdb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fabdb-119">Requirements</span></span>



| <span data-ttu-id="fabdb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fabdb-120">Requirement</span></span> | <span data-ttu-id="fabdb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fabdb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fabdb-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fabdb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fabdb-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fabdb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fabdb-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fabdb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fabdb-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fabdb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fabdb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fabdb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fabdb-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fabdb-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fabdb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fabdb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabdb-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fabdb-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
