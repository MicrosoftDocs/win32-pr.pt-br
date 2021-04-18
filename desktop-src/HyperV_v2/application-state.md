---
description: Especifica o estado de integridade de um aplicativo.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Enumeração de APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753298"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="e4dee-103">Enumeração de estado do aplicativo \_</span><span class="sxs-lookup"><span data-stu-id="e4dee-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="e4dee-104">Especifica o estado de integridade de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4dee-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4dee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4dee-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="e4dee-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e4dee-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4dee-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span><span class="sxs-lookup"><span data-stu-id="e4dee-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="e4dee-108">O estado do aplicativo é íntegro.</span><span class="sxs-lookup"><span data-stu-id="e4dee-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="e4dee-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span><span class="sxs-lookup"><span data-stu-id="e4dee-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="e4dee-110">O estado do aplicativo é crítico.</span><span class="sxs-lookup"><span data-stu-id="e4dee-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4dee-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4dee-111">Remarks</span></span>

<span data-ttu-id="e4dee-112">Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e4dee-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4dee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4dee-113">Requirements</span></span>



| <span data-ttu-id="e4dee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4dee-114">Requirement</span></span> | <span data-ttu-id="e4dee-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e4dee-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4dee-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4dee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4dee-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e4dee-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="e4dee-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4dee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4dee-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e4dee-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4dee-120">Versão</span><span class="sxs-lookup"><span data-stu-id="e4dee-120">Version</span></span><br/>                  | <span data-ttu-id="e4dee-121">Componentes de integração do Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4dee-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="e4dee-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4dee-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4dee-123"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4dee-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4dee-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4dee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4dee-125">**Setapplicationstate**</span><span class="sxs-lookup"><span data-stu-id="e4dee-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




