---
description: A \_ estrutura informações sobre o driver \_ 1 identifica um driver de impressora.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Estrutura de DRIVER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791603"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="7ced0-103">\_Estrutura informações do driver \_ 1</span><span class="sxs-lookup"><span data-stu-id="7ced0-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="7ced0-104">A **estrutura \_ informações \_ sobre o driver 1** identifica um driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="7ced0-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ced0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ced0-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="7ced0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7ced0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ced0-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="7ced0-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="7ced0-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="7ced0-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ced0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ced0-109">Requirements</span></span>



| <span data-ttu-id="7ced0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ced0-110">Requirement</span></span> | <span data-ttu-id="7ced0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7ced0-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ced0-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ced0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7ced0-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ced0-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ced0-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ced0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7ced0-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ced0-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ced0-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7ced0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ced0-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ced0-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7ced0-118">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7ced0-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ced0-119">**\_ Informações do driver \_ \_ 1W** (Unicode) e **\_ info do driver \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7ced0-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="7ced0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ced0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ced0-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="7ced0-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7ced0-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="7ced0-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7ced0-123">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="7ced0-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




