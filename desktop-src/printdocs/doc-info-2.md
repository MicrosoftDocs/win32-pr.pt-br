---
description: A \_ estrutura info \_ 2 do documento descreve um documento que será impresso.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Estrutura de DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760518"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="3d453-103">Estrutura de informações do documento \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="3d453-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="3d453-104">A **estrutura \_ info \_ 2** do documento descreve um documento que será impresso.</span><span class="sxs-lookup"><span data-stu-id="3d453-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d453-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d453-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="3d453-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3d453-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d453-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="3d453-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="3d453-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do documento.</span><span class="sxs-lookup"><span data-stu-id="3d453-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="3d453-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="3d453-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="3d453-110">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d453-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="3d453-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="3d453-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="3d453-112">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar o documento.</span><span class="sxs-lookup"><span data-stu-id="3d453-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="3d453-113">**dwMode**</span><span class="sxs-lookup"><span data-stu-id="3d453-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="3d453-114">Informa ao spooler de impressão a natureza dos dados a serem seguidos.</span><span class="sxs-lookup"><span data-stu-id="3d453-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="3d453-115">Se esse valor for zero, o spooler de impressão tratará os dados enviados por chamadas subsequentes para [**WritePrinter**](writeprinter.md) como um trabalho de impressão normal (se ele for ou não colocado no spool, depende da propriedade da impressora).</span><span class="sxs-lookup"><span data-stu-id="3d453-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="3d453-116">Se esse valor for um \_ canal de di, apenas um canal de comunicação será aberto.</span><span class="sxs-lookup"><span data-stu-id="3d453-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="3d453-117">Nesse caso, os dados passados para as chamadas subsequentes para **WritePrinter** são enviados para a impressora ou chamadas subsequentes para [**ReadPrinter**](readprinter.md) recuperar dados da impressora.</span><span class="sxs-lookup"><span data-stu-id="3d453-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="3d453-118">Esse modo permanece efetivo até que [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="3d453-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="3d453-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="3d453-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="3d453-120">Reservado para uso interno; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3d453-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d453-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d453-121">Requirements</span></span>



| <span data-ttu-id="3d453-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d453-122">Requirement</span></span> | <span data-ttu-id="3d453-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3d453-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d453-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d453-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d453-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d453-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3d453-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d453-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d453-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d453-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3d453-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d453-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d453-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d453-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d453-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3d453-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d453-131">**\_ Informações do documento \_ \_ 2W** (Unicode) e **\_ info do documento \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3d453-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="3d453-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d453-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d453-133">Impressão</span><span class="sxs-lookup"><span data-stu-id="3d453-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3d453-134">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3d453-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3d453-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="3d453-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="3d453-136">**ReadPrinter**</span><span class="sxs-lookup"><span data-stu-id="3d453-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="3d453-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3d453-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="3d453-138">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3d453-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




