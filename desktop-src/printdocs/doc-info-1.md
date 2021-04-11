---
description: A \_ estrutura info \_ 1 do documento descreve um documento que será impresso.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Estrutura de DOC_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169348"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="8f011-103">Estrutura de informações do documento \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="8f011-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="8f011-104">A **estrutura \_ info \_ 1** do documento descreve um documento que será impresso.</span><span class="sxs-lookup"><span data-stu-id="8f011-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f011-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f011-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="8f011-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8f011-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f011-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="8f011-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="8f011-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do documento.</span><span class="sxs-lookup"><span data-stu-id="8f011-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="8f011-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="8f011-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="8f011-110">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="8f011-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="8f011-111">Para imprimir em uma impressora, defina como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8f011-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8f011-112">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="8f011-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="8f011-113">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar o documento.</span><span class="sxs-lookup"><span data-stu-id="8f011-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f011-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f011-114">Requirements</span></span>



| <span data-ttu-id="8f011-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f011-115">Requirement</span></span> | <span data-ttu-id="8f011-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8f011-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f011-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f011-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f011-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f011-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f011-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f011-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f011-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f011-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f011-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f011-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f011-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f011-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8f011-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8f011-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8f011-124">**\_ Informações do documento \_ \_ 1W** (Unicode) e **\_ info do documento \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8f011-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="8f011-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f011-126">Impressão</span><span class="sxs-lookup"><span data-stu-id="8f011-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f011-127">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="8f011-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8f011-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f011-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




