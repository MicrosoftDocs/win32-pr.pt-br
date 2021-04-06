---
description: Define o brilho de vídeo de um monitor de computador.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Método WmiSetBrightness da classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011237"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="18a3f-103">Método WmiSetBrightness da classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="18a3f-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="18a3f-104">O método **WmiSetBrightness** define o brilho de vídeo de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="18a3f-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18a3f-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="18a3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18a3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a3f-107">*Tempo Limite*</span><span class="sxs-lookup"><span data-stu-id="18a3f-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="18a3f-108">Tempo limite, em segundos.</span><span class="sxs-lookup"><span data-stu-id="18a3f-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="18a3f-109">*Brightness*</span><span class="sxs-lookup"><span data-stu-id="18a3f-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="18a3f-110">Brilho, em porcentagem.</span><span class="sxs-lookup"><span data-stu-id="18a3f-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18a3f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18a3f-111">Return value</span></span>

<span data-ttu-id="18a3f-112">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="18a3f-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="18a3f-113">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="18a3f-113">Any other number indicates an error.</span></span> <span data-ttu-id="18a3f-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="18a3f-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="18a3f-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18a3f-115">Examples</span></span>

<span data-ttu-id="18a3f-116">Para obter uma discussão estendida sobre como recuperar e definir o brilho do monitor, consulte o tópico do blog [usar o PowerShell para relatar e definir o brilho de monitoramento](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) .</span><span class="sxs-lookup"><span data-stu-id="18a3f-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="18a3f-117">O exemplo do PowerShell a seguir define o brilho do monitor para 50%.</span><span class="sxs-lookup"><span data-stu-id="18a3f-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="18a3f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18a3f-118">Requirements</span></span>



| <span data-ttu-id="18a3f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a3f-119">Requirement</span></span> | <span data-ttu-id="18a3f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="18a3f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18a3f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a3f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18a3f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18a3f-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18a3f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a3f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18a3f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18a3f-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18a3f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="18a3f-125">Namespace</span></span><br/>                | <span data-ttu-id="18a3f-126">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="18a3f-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="18a3f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="18a3f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18a3f-128"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18a3f-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="18a3f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="18a3f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18a3f-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18a3f-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a3f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="18a3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a3f-132">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="18a3f-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="18a3f-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="18a3f-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

