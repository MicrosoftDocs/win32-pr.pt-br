---
description: A \_ estrutura informações do monitor \_ 2 identifica um monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Estrutura de MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663207"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="f8e32-103">Estrutura de informações de MONITOR \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="f8e32-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="f8e32-104">A **estrutura \_ informações \_ do monitor 2** identifica um monitor.</span><span class="sxs-lookup"><span data-stu-id="f8e32-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8e32-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f8e32-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f8e32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8e32-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="f8e32-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="f8e32-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do monitor.</span><span class="sxs-lookup"><span data-stu-id="f8e32-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="f8e32-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f8e32-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="f8e32-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o monitor foi gravado (por exemplo, Windows NT x86, Windows IA64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="f8e32-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="f8e32-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="f8e32-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="f8e32-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que é o nome da DLL do monitor.</span><span class="sxs-lookup"><span data-stu-id="f8e32-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8e32-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e32-113">Requirements</span></span>



| <span data-ttu-id="f8e32-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e32-114">Requirement</span></span> | <span data-ttu-id="f8e32-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f8e32-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e32-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e32-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e32-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8e32-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8e32-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e32-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e32-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8e32-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8e32-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8e32-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e32-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e32-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8e32-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f8e32-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8e32-123">**\_ Monitor de \_ informações \_ 2W** (Unicode) e **\_ informações de monitor \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8e32-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f8e32-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8e32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e32-125">Impressão</span><span class="sxs-lookup"><span data-stu-id="f8e32-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8e32-126">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f8e32-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f8e32-127">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="f8e32-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="f8e32-128">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="f8e32-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="f8e32-129">**Informações do MONITOR \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f8e32-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




