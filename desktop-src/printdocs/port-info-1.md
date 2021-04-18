---
description: A \_ estrutura informações sobre a porta \_ 1 identifica uma porta de impressora com suporte.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Estrutura de PORT_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765785"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="0c36c-103">Estrutura de informações de porta \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c36c-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="0c36c-104">A **estrutura \_ informações \_ sobre a porta 1** identifica uma porta de impressora com suporte.</span><span class="sxs-lookup"><span data-stu-id="0c36c-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c36c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c36c-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="0c36c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0c36c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c36c-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="0c36c-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="0c36c-108">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica uma porta de impressora com suporte (por exemplo, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="0c36c-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c36c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c36c-109">Requirements</span></span>



| <span data-ttu-id="0c36c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c36c-110">Requirement</span></span> | <span data-ttu-id="0c36c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0c36c-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c36c-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c36c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0c36c-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c36c-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0c36c-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c36c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0c36c-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c36c-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0c36c-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0c36c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c36c-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c36c-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0c36c-118">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0c36c-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0c36c-119">Informações de **\_ porta \_ \_ 1W** (Unicode) e **\_ informações de porta \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0c36c-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="0c36c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c36c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c36c-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="0c36c-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0c36c-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0c36c-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="0c36c-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="0c36c-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




