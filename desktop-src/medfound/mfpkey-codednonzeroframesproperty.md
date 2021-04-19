---
description: Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Propriedade MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812237"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="1850d-103">\_Propriedade MFPKEY CODEDNONZEROFRAMES</span><span class="sxs-lookup"><span data-stu-id="1850d-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="1850d-104">Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.</span><span class="sxs-lookup"><span data-stu-id="1850d-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1850d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1850d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1850d-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1850d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1850d-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1850d-107">Data Type</span></span>

<span data-ttu-id="1850d-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="1850d-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="1850d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1850d-109">Remarks</span></span>

<span data-ttu-id="1850d-110">Esse valor é igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos quaisquer quadros que foram descartados devido a restrições de taxa de bits, menos quaisquer quadros de zero byte.</span><span class="sxs-lookup"><span data-stu-id="1850d-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="1850d-111">Você pode obter esse valor depois de terminar de passar amostras.</span><span class="sxs-lookup"><span data-stu-id="1850d-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="1850d-112">Quadros de zero byte podem ser criados para quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="1850d-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="1850d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1850d-113">Requirements</span></span>



| <span data-ttu-id="1850d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1850d-114">Requirement</span></span> | <span data-ttu-id="1850d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1850d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1850d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1850d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1850d-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1850d-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1850d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1850d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1850d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1850d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1850d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1850d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1850d-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1850d-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1850d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1850d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1850d-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1850d-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
