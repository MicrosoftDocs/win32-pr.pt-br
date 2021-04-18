---
description: Especifica se o codificador deve usar um tamanho de quadro preferencial fornecido no número de amostras por quadro.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Propriedade MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760531"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="45c61-103">MFPKEY \_ solicitando \_ uma \_ Propriedade frameize</span><span class="sxs-lookup"><span data-stu-id="45c61-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="45c61-104">Especifica se o codificador deve usar um tamanho de quadro preferencial fornecido no número de amostras por quadro.</span><span class="sxs-lookup"><span data-stu-id="45c61-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="45c61-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="45c61-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="45c61-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="45c61-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="45c61-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="45c61-107">Data Type</span></span>

<span data-ttu-id="45c61-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="45c61-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="45c61-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c61-109">Remarks</span></span>

<span data-ttu-id="45c61-110">Para especificar um tamanho de quadro preferencial, defina as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="45c61-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="45c61-111">Defina **MFPKEY \_ solicitando \_ um \_ frameize** como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="45c61-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="45c61-112">Defina [**MFPKEY \_ de \_ quadros preferenciais**](mfpkey-preferred-framesizeproperty.md) para o número de amostras desejado em cada quadro.</span><span class="sxs-lookup"><span data-stu-id="45c61-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c61-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c61-113">Requirements</span></span>



| <span data-ttu-id="45c61-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c61-114">Requirement</span></span> | <span data-ttu-id="45c61-115">Valor</span><span class="sxs-lookup"><span data-stu-id="45c61-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45c61-116">Cliente</span><span class="sxs-lookup"><span data-stu-id="45c61-116">Client</span></span><br/> | <span data-ttu-id="45c61-117">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="45c61-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="45c61-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45c61-118">Header</span></span><br/> | <dl> <span data-ttu-id="45c61-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c61-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c61-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c61-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c61-121">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45c61-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
