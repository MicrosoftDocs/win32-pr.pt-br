---
description: A \_ estrutura info do multiprocessador informações \_ 1 especifica o nome de um processador de impressão instalado.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Estrutura de PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781414"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="e761d-103">Estrutura informações do multiprocessador \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="e761d-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="e761d-104">A estrutura **info do multiprocessador \_ informações \_ 1** especifica o nome de um processador de impressão instalado.</span><span class="sxs-lookup"><span data-stu-id="e761d-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e761d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e761d-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e761d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e761d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e761d-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="e761d-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="e761d-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um processador de impressão instalado.</span><span class="sxs-lookup"><span data-stu-id="e761d-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e761d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e761d-109">Requirements</span></span>



| <span data-ttu-id="e761d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e761d-110">Requirement</span></span> | <span data-ttu-id="e761d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e761d-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e761d-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e761d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e761d-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e761d-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e761d-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e761d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e761d-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e761d-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e761d-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e761d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e761d-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e761d-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e761d-118">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e761d-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e761d-119">Informações de **\_ \_ \_ 1W** (Unicode) e informações de **\_ multiprocessadores \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e761d-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e761d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e761d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e761d-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="e761d-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e761d-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e761d-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e761d-123">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="e761d-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




