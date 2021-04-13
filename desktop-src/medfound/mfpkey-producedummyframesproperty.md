---
description: Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Propriedade MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165378"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="de6ea-103">\_Propriedade MFPKEY PRODUCEDUMMYFRAMES</span><span class="sxs-lookup"><span data-stu-id="de6ea-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="de6ea-104">Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="de6ea-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="de6ea-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="de6ea-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="de6ea-106">g \_ wszWMVCProduceDummyFrames</span><span class="sxs-lookup"><span data-stu-id="de6ea-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="de6ea-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="de6ea-107">Data Type</span></span>

<span data-ttu-id="de6ea-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="de6ea-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="de6ea-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="de6ea-109">Default Value</span></span>

<span data-ttu-id="de6ea-110">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="de6ea-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="de6ea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="de6ea-111">Remarks</span></span>

<span data-ttu-id="de6ea-112">Se esse valor for VARIANT \_ false, o codec não colocará nenhum dado no fluxo de bits para quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="de6ea-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="de6ea-113">Quadros fictícios podem ser importantes em aplicativos em que os números de quadro são persistidos.</span><span class="sxs-lookup"><span data-stu-id="de6ea-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="de6ea-114">Um exemplo comum é quando os códigos de tempo SMPTE são mantidos para conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="de6ea-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="de6ea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de6ea-115">Requirements</span></span>



| <span data-ttu-id="de6ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de6ea-116">Requirement</span></span> | <span data-ttu-id="de6ea-117">Valor</span><span class="sxs-lookup"><span data-stu-id="de6ea-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de6ea-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de6ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de6ea-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="de6ea-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de6ea-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de6ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de6ea-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de6ea-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de6ea-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de6ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de6ea-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de6ea-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de6ea-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="de6ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6ea-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de6ea-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




