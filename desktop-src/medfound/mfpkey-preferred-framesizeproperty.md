---
description: Especifica o número preferencial de amostras por quadro.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Propriedade MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770592"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="195f9-103">\_ \_ Propriedade frameize de MFPKEY preferencial</span><span class="sxs-lookup"><span data-stu-id="195f9-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="195f9-104">Especifica o número preferencial de amostras por quadro.</span><span class="sxs-lookup"><span data-stu-id="195f9-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="195f9-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="195f9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="195f9-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="195f9-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="195f9-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="195f9-107">Data Type</span></span>

<span data-ttu-id="195f9-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="195f9-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="195f9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="195f9-109">Remarks</span></span>

<span data-ttu-id="195f9-110">Para especificar um tamanho de quadro preferencial, defina as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="195f9-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="195f9-111">Defina [**MFPKEY \_ solicitando \_ um \_ frameize**](mfpkey-requesting-a-framesizeproperty.md) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="195f9-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="195f9-112">Defina **MFPKEY \_ de \_ quadros preferenciais** para o número de amostras desejado em cada quadro.</span><span class="sxs-lookup"><span data-stu-id="195f9-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="195f9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="195f9-113">Requirements</span></span>



| <span data-ttu-id="195f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="195f9-114">Requirement</span></span> | <span data-ttu-id="195f9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="195f9-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="195f9-116">Cliente</span><span class="sxs-lookup"><span data-stu-id="195f9-116">Client</span></span><br/> | <span data-ttu-id="195f9-117">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="195f9-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="195f9-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="195f9-118">Header</span></span><br/> | <dl> <span data-ttu-id="195f9-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="195f9-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195f9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="195f9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195f9-121">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="195f9-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
