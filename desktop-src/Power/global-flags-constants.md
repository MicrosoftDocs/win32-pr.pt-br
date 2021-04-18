---
description: As constantes de sinalizadores globais são usadas para habilitar ou desabilitar opções de política de energia de usuário.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de sinalizadores globais (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783247"
---
# <a name="global-flags-constants"></a><span data-ttu-id="f4f5c-103">Constantes de sinalizadores globais</span><span class="sxs-lookup"><span data-stu-id="f4f5c-103">Global Flags Constants</span></span>

<span data-ttu-id="f4f5c-104">As constantes de sinalizadores globais são usadas para habilitar ou desabilitar opções de política de energia de usuário.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="f4f5c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f4f5c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="f4f5c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4f5c-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="f4f5c-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="f4f5c-108">Habilita ou desabilita várias exibições de bateria no medidor de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="f4f5c-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="f4f5c-110">Habilita ou desabilita a exigência de logon de senha quando o sistema é retomado do modo de espera ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="f4f5c-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="f4f5c-112">Habilita ou desabilita o ícone de medidor de bateria na bandeja do sistema.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="f4f5c-113">Quando esse sinalizador é removido, o ícone de medidor de bateria não é exibido.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="f4f5c-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="f4f5c-115">Habilita ou desabilita o suporte para o esmaecimento da tela de vídeo quando o sistema muda de execução em energia CA para em execução com energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="f4f5c-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="f4f5c-117">Habilita ou desabilita o suporte a Wake on Ring.</span><span class="sxs-lookup"><span data-stu-id="f4f5c-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="f4f5c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f5c-118">Requirements</span></span>



| <span data-ttu-id="f4f5c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f5c-119">Requirement</span></span> | <span data-ttu-id="f4f5c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f5c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f5c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4f5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f5c-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f4f5c-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f4f5c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4f5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f5c-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4f5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4f5c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4f5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4f5c-126"><dt>PowrProf. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f5c-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f5c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4f5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f5c-128">**\_política de \_ energia de usuário global \_**</span><span class="sxs-lookup"><span data-stu-id="f4f5c-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




