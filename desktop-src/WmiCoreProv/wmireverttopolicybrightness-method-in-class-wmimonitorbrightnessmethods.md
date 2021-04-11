---
description: O método WmiRevertToPolicyBrightness é usado para reverter o brilho para a configuração de política. Esse método não tem nenhum efeito nas configurações de brilho do ALS.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Método WmiRevertToPolicyBrightness da classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170008"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="09979-104">Método WmiRevertToPolicyBrightness da classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="09979-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="09979-105">O método **WmiRevertToPolicyBrightness** é usado para reverter o brilho para a configuração de política.</span><span class="sxs-lookup"><span data-stu-id="09979-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="09979-106">Esse método não tem nenhum efeito nas configurações de brilho do ALS.</span><span class="sxs-lookup"><span data-stu-id="09979-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="09979-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09979-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="09979-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09979-108">Parameters</span></span>

<span data-ttu-id="09979-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09979-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09979-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09979-110">Return value</span></span>

<span data-ttu-id="09979-111">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="09979-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="09979-112">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="09979-112">Any other number indicates an error.</span></span> <span data-ttu-id="09979-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="09979-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="09979-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09979-114">Requirements</span></span>



| <span data-ttu-id="09979-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09979-115">Requirement</span></span> | <span data-ttu-id="09979-116">Valor</span><span class="sxs-lookup"><span data-stu-id="09979-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09979-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09979-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09979-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09979-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09979-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09979-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09979-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09979-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09979-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="09979-121">Namespace</span></span><br/>                | <span data-ttu-id="09979-122">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="09979-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="09979-123">MOF</span><span class="sxs-lookup"><span data-stu-id="09979-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09979-124"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09979-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="09979-125">DLL</span><span class="sxs-lookup"><span data-stu-id="09979-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09979-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09979-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09979-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="09979-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09979-128">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="09979-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="09979-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="09979-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

