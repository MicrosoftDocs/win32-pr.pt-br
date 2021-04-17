---
description: Representa opções de impressora.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Estrutura de PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770652"
---
# <a name="printer_options-structure"></a><span data-ttu-id="b604c-103">Estrutura de opções de impressora \_</span><span class="sxs-lookup"><span data-stu-id="b604c-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="b604c-104">Representa opções de impressora.</span><span class="sxs-lookup"><span data-stu-id="b604c-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="b604c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b604c-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="b604c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b604c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b604c-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="b604c-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b604c-108">O tamanho da estrutura **de \_ Opções da impressora** .</span><span class="sxs-lookup"><span data-stu-id="b604c-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b604c-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b604c-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b604c-110">Um conjunto de [**\_ \_ sinalizadores de opção de impressora**](printer-option-flags.md) que especifica como o identificador para uma impressora retornada por [**OpenPrinter2**](openprinter2.md) será usado por outras funções.</span><span class="sxs-lookup"><span data-stu-id="b604c-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b604c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b604c-111">Requirements</span></span>



| <span data-ttu-id="b604c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b604c-112">Requirement</span></span> | <span data-ttu-id="b604c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b604c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b604c-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b604c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b604c-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b604c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b604c-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b604c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b604c-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b604c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b604c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b604c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b604c-119"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b604c-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b604c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b604c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b604c-121">Impressão</span><span class="sxs-lookup"><span data-stu-id="b604c-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b604c-122">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b604c-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b604c-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="b604c-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="b604c-124">**\_sinalizadores de opção de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="b604c-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




