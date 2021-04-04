---
description: Especifica o cache de um identificador para uma impressora aberta com OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumeração de PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171026"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="175bb-103">Enumeração de sinalizadores de \_ opção de impressora \_</span><span class="sxs-lookup"><span data-stu-id="175bb-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="175bb-104">Especifica o cache de um identificador para uma impressora aberta com [**OpenPrinter2**](openprinter2.md).</span><span class="sxs-lookup"><span data-stu-id="175bb-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="175bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="175bb-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="175bb-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="175bb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="175bb-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**opção de impressora \_ \_ sem \_ cache**</span><span class="sxs-lookup"><span data-stu-id="175bb-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="175bb-108">O identificador não está armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="175bb-108">The handle is not cached.</span></span> <span data-ttu-id="175bb-109">Todas as funções aplicadas a um identificador retornado pelo [**OpenPrinter2**](openprinter2.md) vão para o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="175bb-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="175bb-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache de opção de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="175bb-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="175bb-111">O identificador é armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="175bb-111">The handle is cached.</span></span> <span data-ttu-id="175bb-112">Todas as funções aplicadas a um identificador retornado por [**OpenPrinter2**](openprinter2.md) vão para o cache local.</span><span class="sxs-lookup"><span data-stu-id="175bb-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="175bb-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**opção da impressora \_ \_ alteração do cliente \_**</span><span class="sxs-lookup"><span data-stu-id="175bb-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="175bb-114">O identificador retornado por [**OpenPrinter2**](openprinter2.md) pode ser usado pelo [**setprinter**](setprinter.md) para renomear a conexão de impressora.</span><span class="sxs-lookup"><span data-stu-id="175bb-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="175bb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="175bb-115">Requirements</span></span>



| <span data-ttu-id="175bb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="175bb-116">Requirement</span></span> | <span data-ttu-id="175bb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="175bb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="175bb-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="175bb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="175bb-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="175bb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="175bb-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="175bb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="175bb-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="175bb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="175bb-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="175bb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="175bb-123"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="175bb-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175bb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="175bb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175bb-125">Impressão</span><span class="sxs-lookup"><span data-stu-id="175bb-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="175bb-126">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="175bb-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="175bb-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="175bb-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="175bb-128">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="175bb-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




