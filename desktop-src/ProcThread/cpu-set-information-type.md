---
description: Representa o tipo de informação na estrutura de \_ informações do conjunto de CPU do sistema \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Enumeração de CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759613"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="ee027-103">\_Enumeração de \_ tipo de informação de conjunto de CPU \_</span><span class="sxs-lookup"><span data-stu-id="ee027-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="ee027-104">Representa o tipo de informação na estrutura [**de \_ \_ \_ informações do conjunto de CPU do sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .</span><span class="sxs-lookup"><span data-stu-id="ee027-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee027-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee027-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ee027-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ee027-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee027-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span><span class="sxs-lookup"><span data-stu-id="ee027-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="ee027-108">A estrutura contém informações de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="ee027-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee027-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee027-109">Requirements</span></span>



| <span data-ttu-id="ee027-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee027-110">Requirement</span></span> | <span data-ttu-id="ee027-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ee027-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee027-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee027-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ee027-113">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ee027-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="ee027-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee027-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ee027-115">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ee027-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee027-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee027-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee027-117"><dt>Processthreadsapi. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee027-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




