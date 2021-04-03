---
description: Fornece informações sobre a conectividade de rede para uma máquina virtual.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Classe Msvm_NetworkConnectionDiagnosticInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 416392702e5bc06e54fe5a23b6784b87e98b7027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922695"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a><span data-ttu-id="3b478-103">\_Classe Msvm NetworkConnectionDiagnosticInformation</span><span class="sxs-lookup"><span data-stu-id="3b478-103">Msvm\_NetworkConnectionDiagnosticInformation class</span></span>

<span data-ttu-id="3b478-104">Fornece informações sobre a conectividade de rede para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b478-104">Provides information about the network connectivity for a virtual machine.</span></span>

<span data-ttu-id="3b478-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3b478-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b478-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b478-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a><span data-ttu-id="3b478-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3b478-107">Members</span></span>

<span data-ttu-id="3b478-108">A classe **Msvm \_ NetworkConnectionDiagnosticInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3b478-108">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="3b478-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b478-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b478-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b478-110">Properties</span></span>

<span data-ttu-id="3b478-111">A classe **Msvm \_ NetworkConnectionDiagnosticInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b478-111">The **Msvm\_NetworkConnectionDiagnosticInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b478-112">**RoundTripTime**</span><span class="sxs-lookup"><span data-stu-id="3b478-112">**RoundTripTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b478-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b478-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b478-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b478-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b478-115">O tempo de ida e volta para a solicitação ping.</span><span class="sxs-lookup"><span data-stu-id="3b478-115">The round trip time for the ping request.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b478-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b478-116">Requirements</span></span>



| <span data-ttu-id="3b478-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b478-117">Requirement</span></span> | <span data-ttu-id="3b478-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3b478-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b478-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b478-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b478-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="3b478-120">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3b478-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b478-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b478-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3b478-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3b478-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b478-123">Namespace</span></span><br/>                | <span data-ttu-id="3b478-124">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3b478-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3b478-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3b478-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b478-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b478-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b478-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b478-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b478-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b478-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




