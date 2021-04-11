---
description: Usado para definir o valor de brilho do sensor de luz ambiente.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Método WmiSetALSBrightness da classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172147"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="10300-103">Método WmiSetALSBrightness da classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="10300-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="10300-104">O método **WmiSetALSBrightness** é usado para definir o valor de brilho do sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="10300-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="10300-105">Se uma substituição de brilho ativa foi estabelecida usando o método [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , essa substituição terá precedência sobre o brilho do ALS definido usando esse método.</span><span class="sxs-lookup"><span data-stu-id="10300-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="10300-106">Para que uma substituição de brilho de ALS habilitada tenha efeito, a política de brilho deve ser revertida usando o método [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="10300-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="10300-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10300-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="10300-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10300-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10300-109">*Brightness*</span><span class="sxs-lookup"><span data-stu-id="10300-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="10300-110">O brilho de ALS como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="10300-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10300-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10300-111">Return value</span></span>

<span data-ttu-id="10300-112">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="10300-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="10300-113">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="10300-113">Any other number indicates an error.</span></span> <span data-ttu-id="10300-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="10300-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="10300-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10300-115">Requirements</span></span>



| <span data-ttu-id="10300-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10300-116">Requirement</span></span> | <span data-ttu-id="10300-117">Valor</span><span class="sxs-lookup"><span data-stu-id="10300-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10300-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10300-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10300-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10300-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="10300-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10300-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10300-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10300-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="10300-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="10300-122">Namespace</span></span><br/>                | <span data-ttu-id="10300-123">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="10300-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="10300-124">MOF</span><span class="sxs-lookup"><span data-stu-id="10300-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10300-125"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10300-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="10300-126">DLL</span><span class="sxs-lookup"><span data-stu-id="10300-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10300-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10300-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10300-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="10300-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10300-129">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="10300-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="10300-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="10300-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

