---
description: A lista a seguir descreve as constantes da política de descarga.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes da política de descarga (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764627"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="eaac9-103">Constantes da política de descarga</span><span class="sxs-lookup"><span data-stu-id="eaac9-103">Discharge Policy Constants</span></span>

<span data-ttu-id="eaac9-104">A lista a seguir descreve as constantes da política de descarga.</span><span class="sxs-lookup"><span data-stu-id="eaac9-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="eaac9-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="eaac9-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="eaac9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="eaac9-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="eaac9-107"><dt>**Descarga \_ POLÍTICA \_ crítica**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eaac9-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="eaac9-108">Quais das configurações de política de descarga da bateria (estruturas do [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) são usadas quando a bateria é descarregada abaixo do limite crítico.</span><span class="sxs-lookup"><span data-stu-id="eaac9-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="eaac9-109"><dt>**Descarga \_ POLÍTICA \_ baixa**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eaac9-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="eaac9-110">Qual das configurações de política de descarga da bateria (estruturas do [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) é usada quando a bateria é descarregada abaixo do limite baixo.</span><span class="sxs-lookup"><span data-stu-id="eaac9-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="eaac9-111"><dt>**Número \_ de \_Políticas de descarga**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eaac9-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="eaac9-112">Número de configurações de política de descarga da bateria (estruturas de [**\_ \_ nível de energia do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) especificadas.</span><span class="sxs-lookup"><span data-stu-id="eaac9-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="eaac9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaac9-113">Requirements</span></span>



| <span data-ttu-id="eaac9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaac9-114">Requirement</span></span> | <span data-ttu-id="eaac9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eaac9-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaac9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaac9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eaac9-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eaac9-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eaac9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaac9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eaac9-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eaac9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="eaac9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eaac9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaac9-121"><dt>WinNT. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaac9-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




