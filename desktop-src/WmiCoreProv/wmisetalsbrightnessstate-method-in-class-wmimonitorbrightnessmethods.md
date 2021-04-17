---
description: Usado para controlar o estado de brilho do sensor de luz ambiente.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Método WmiSetALSBrightnessState da classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811397"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="ee247-103">Método WmiSetALSBrightnessState da classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="ee247-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="ee247-104">O método **WmiSetALSBrightnessState** é usado para controlar o estado de brilho do sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="ee247-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="ee247-105">Se uma substituição de brilho ativa foi estabelecida usando o método [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , essa substituição terá precedência sobre o brilho do ALS definido usando esse método.</span><span class="sxs-lookup"><span data-stu-id="ee247-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="ee247-106">Para que uma substituição de brilho de ALS habilitada tenha efeito, a política de brilho deve ser revertida usando o método [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="ee247-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee247-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee247-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="ee247-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee247-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee247-109">*State*</span><span class="sxs-lookup"><span data-stu-id="ee247-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="ee247-110">Estado de brilho do ALS.</span><span class="sxs-lookup"><span data-stu-id="ee247-110">ALS brightness state.</span></span> <span data-ttu-id="ee247-111">False desabilita a substituição de brilho de ALS e True habilita-a.</span><span class="sxs-lookup"><span data-stu-id="ee247-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee247-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee247-112">Return value</span></span>

<span data-ttu-id="ee247-113">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="ee247-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="ee247-114">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="ee247-114">Any other number indicates an error.</span></span> <span data-ttu-id="ee247-115">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ee247-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee247-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee247-116">Requirements</span></span>



| <span data-ttu-id="ee247-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee247-117">Requirement</span></span> | <span data-ttu-id="ee247-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ee247-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee247-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee247-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee247-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee247-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ee247-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee247-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee247-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee247-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ee247-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee247-123">Namespace</span></span><br/>                | <span data-ttu-id="ee247-124">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="ee247-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ee247-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ee247-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee247-126"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee247-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee247-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee247-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee247-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee247-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee247-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee247-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee247-130">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="ee247-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="ee247-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ee247-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

