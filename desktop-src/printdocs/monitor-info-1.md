---
description: A \_ estrutura informações do monitor \_ 1 identifica um monitor instalado.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Estrutura de MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783743"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="130ad-103">MONITORAR \_ a \_ estrutura de informações 1</span><span class="sxs-lookup"><span data-stu-id="130ad-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="130ad-104">A **estrutura \_ informações \_ do monitor 1** identifica um monitor instalado.</span><span class="sxs-lookup"><span data-stu-id="130ad-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="130ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="130ad-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="130ad-106">Membros</span><span class="sxs-lookup"><span data-stu-id="130ad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="130ad-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="130ad-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="130ad-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica um monitor instalado.</span><span class="sxs-lookup"><span data-stu-id="130ad-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="130ad-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="130ad-109">Requirements</span></span>



| <span data-ttu-id="130ad-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="130ad-110">Requirement</span></span> | <span data-ttu-id="130ad-111">Valor</span><span class="sxs-lookup"><span data-stu-id="130ad-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130ad-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="130ad-112">Minimum supported client</span></span><br/> | <span data-ttu-id="130ad-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="130ad-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="130ad-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="130ad-114">Minimum supported server</span></span><br/> | <span data-ttu-id="130ad-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="130ad-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="130ad-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="130ad-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="130ad-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="130ad-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="130ad-118">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="130ad-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="130ad-119">Informações de monitor **\_ \_ \_ 1W** (Unicode) e **\_ informações de monitor \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="130ad-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="130ad-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="130ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130ad-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="130ad-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="130ad-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="130ad-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="130ad-123">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="130ad-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="130ad-124">**Informações do MONITOR \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="130ad-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




