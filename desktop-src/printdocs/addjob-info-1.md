---
description: A \_ estrutura ADDJOB info \_ 1 identifica um trabalho de impressão, bem como o diretório e o arquivo em que um aplicativo pode armazenar esse trabalho.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Estrutura de ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171716"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="46a40-103">Estrutura de informações de ADDJOB \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="46a40-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="46a40-104">A estrutura **ADDJOB \_ info \_ 1** identifica um trabalho de impressão, bem como o diretório e o arquivo em que um aplicativo pode armazenar esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="46a40-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46a40-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="46a40-106">Membros</span><span class="sxs-lookup"><span data-stu-id="46a40-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46a40-107">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="46a40-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="46a40-108">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho e o nome do arquivo que o aplicativo pode usar para armazenar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="46a40-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="46a40-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="46a40-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="46a40-110">Um identificador para o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="46a40-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46a40-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46a40-111">Requirements</span></span>



| <span data-ttu-id="46a40-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a40-112">Requirement</span></span> | <span data-ttu-id="46a40-113">Valor</span><span class="sxs-lookup"><span data-stu-id="46a40-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a40-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a40-114">Minimum supported client</span></span><br/> | <span data-ttu-id="46a40-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46a40-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46a40-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a40-116">Minimum supported server</span></span><br/> | <span data-ttu-id="46a40-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46a40-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46a40-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46a40-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="46a40-119"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46a40-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="46a40-120">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="46a40-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46a40-121">**\_ ADDJOB \_ info \_ 1W** (Unicode) e **\_ ADDJOB \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="46a40-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="46a40-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="46a40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a40-123">Impressão</span><span class="sxs-lookup"><span data-stu-id="46a40-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="46a40-124">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="46a40-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="46a40-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="46a40-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




