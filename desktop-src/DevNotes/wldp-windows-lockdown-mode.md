---
description: Descreve os modos seguros (S) para um dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumeração de WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755273"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="731fd-103">\_Enumeração do \_ modo de bloqueio do Windows WLDP \_</span><span class="sxs-lookup"><span data-stu-id="731fd-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="731fd-104">Descreve os modos seguros (S) para um dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="731fd-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="731fd-105">Usado principalmente em [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span><span class="sxs-lookup"><span data-stu-id="731fd-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="731fd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="731fd-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="731fd-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="731fd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="731fd-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ desbloqueado**</span><span class="sxs-lookup"><span data-stu-id="731fd-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="731fd-109">Sala.</span><span class="sxs-lookup"><span data-stu-id="731fd-109">Unlocked.</span></span> <span data-ttu-id="731fd-110">Usado principalmente para dispositivos Windows sem o modo S.</span><span class="sxs-lookup"><span data-stu-id="731fd-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="731fd-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**\_avaliação do \_ modo de bloqueio do Windows WLDP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="731fd-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="731fd-112">Avaliação.</span><span class="sxs-lookup"><span data-stu-id="731fd-112">Trial.</span></span> <span data-ttu-id="731fd-113">Usado principalmente para um dispositivo de avaliação do Windows 10 com o modo S.</span><span class="sxs-lookup"><span data-stu-id="731fd-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="731fd-114">O modo de avaliação é um caso especial para dispositivos Windows 10 com o modo S: as políticas são impostas, mas não há nenhuma proteção de proversão para a imposição da política.</span><span class="sxs-lookup"><span data-stu-id="731fd-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="731fd-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="731fd-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="731fd-116">Bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="731fd-116">Locked.</span></span> <span data-ttu-id="731fd-117">Usado principalmente para um dispositivo Windows 10 com o modo S.</span><span class="sxs-lookup"><span data-stu-id="731fd-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="731fd-118">Um dispositivo bloqueado imporá as políticas de proteção de dispositivo assinadas enviadas com a imagem do sistema operacional do Windows 10 com o modo S.</span><span class="sxs-lookup"><span data-stu-id="731fd-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="731fd-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**\_modo de bloqueio do Windows WLDP \_ \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="731fd-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="731fd-120">O valor máximo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="731fd-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="731fd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="731fd-121">Requirements</span></span>



| <span data-ttu-id="731fd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="731fd-122">Requirement</span></span> | <span data-ttu-id="731fd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="731fd-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="731fd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="731fd-124">Header</span></span><br/> | <dl> <span data-ttu-id="731fd-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="731fd-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




