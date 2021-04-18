---
description: Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens. Leitura/gravação.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Propriedade MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781231"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="db5e4-104">\_Propriedade MFPKEY CHECKDATACONSISTENCY2P</span><span class="sxs-lookup"><span data-stu-id="db5e4-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="db5e4-105">Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="db5e4-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="db5e4-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="db5e4-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="db5e4-107">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="db5e4-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="db5e4-108">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="db5e4-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="db5e4-109">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="db5e4-109">Data Type</span></span>

<span data-ttu-id="db5e4-110">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="db5e4-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="db5e4-111">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="db5e4-111">Default Value</span></span>

<span data-ttu-id="db5e4-112">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="db5e4-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="db5e4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="db5e4-113">Remarks</span></span>

<span data-ttu-id="db5e4-114">Se você deixar essa propriedade com seu valor padrão de **Variant \_ true**, o codificador verificará se as amostras de entrada correspondem entre as duas passagens e falhará se detectar uma discrepância.</span><span class="sxs-lookup"><span data-stu-id="db5e4-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="db5e4-115">O cenário principal que leva a uma discrepância é quando a entrada vem de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db5e4-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5e4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db5e4-116">Requirements</span></span>



| <span data-ttu-id="db5e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5e4-117">Requirement</span></span> | <span data-ttu-id="db5e4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db5e4-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db5e4-119">Cliente</span><span class="sxs-lookup"><span data-stu-id="db5e4-119">Client</span></span><br/> | <span data-ttu-id="db5e4-120">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="db5e4-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="db5e4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db5e4-121">Header</span></span><br/> | <dl> <span data-ttu-id="db5e4-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5e4-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5e4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="db5e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5e4-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db5e4-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
