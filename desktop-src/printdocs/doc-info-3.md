---
description: A \_ estrutura informações do documento \_ 3 descreve um documento que será impresso.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Estrutura de DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798488"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="9db1d-103">Estrutura de informações do documento \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="9db1d-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="9db1d-104">A **estrutura \_ informações \_ do documento 3** descreve um documento que será impresso.</span><span class="sxs-lookup"><span data-stu-id="9db1d-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db1d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9db1d-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="9db1d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9db1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9db1d-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="9db1d-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="9db1d-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do documento.</span><span class="sxs-lookup"><span data-stu-id="9db1d-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="9db1d-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="9db1d-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="9db1d-110">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="9db1d-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="9db1d-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="9db1d-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9db1d-112">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar o documento.</span><span class="sxs-lookup"><span data-stu-id="9db1d-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="9db1d-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="9db1d-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9db1d-114">Flags.</span><span class="sxs-lookup"><span data-stu-id="9db1d-114">Flags.</span></span> <span data-ttu-id="9db1d-115">No momento, ele pode ser **nulo** ou o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9db1d-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="9db1d-116">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="9db1d-116">Flag</span></span>                 | <span data-ttu-id="9db1d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9db1d-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db1d-118">\_gravação de MEMORYMAP de di \_</span><span class="sxs-lookup"><span data-stu-id="9db1d-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="9db1d-119">Faz com que o [**StartDocPrinter**](startdocprinter.md) não use [**AddJob**](addjob.md) e [**ScheduleJob**](schedulejob.md) para impressão local.</span><span class="sxs-lookup"><span data-stu-id="9db1d-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9db1d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9db1d-120">Remarks</span></span>

<span data-ttu-id="9db1d-121">A \_ configuração de gravação de MEMORYMAP de di \_ no **documento \_ informações \_ 3** é uma otimização.</span><span class="sxs-lookup"><span data-stu-id="9db1d-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="9db1d-122">Isso permite que o GDI mapeie arquivos de spool no aplicativo e acelere a gravação.</span><span class="sxs-lookup"><span data-stu-id="9db1d-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db1d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9db1d-123">Requirements</span></span>



| <span data-ttu-id="9db1d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db1d-124">Requirement</span></span> | <span data-ttu-id="9db1d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9db1d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db1d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db1d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9db1d-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9db1d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9db1d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db1d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9db1d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9db1d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9db1d-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9db1d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db1d-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9db1d-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9db1d-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9db1d-133">**\_ Informações do documento \_ \_ 3W** (Unicode) e **\_ info do documento \_ \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9db1d-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="9db1d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9db1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db1d-135">Impressão</span><span class="sxs-lookup"><span data-stu-id="9db1d-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9db1d-136">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9db1d-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9db1d-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="9db1d-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="9db1d-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="9db1d-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="9db1d-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9db1d-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




