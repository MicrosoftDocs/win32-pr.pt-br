---
description: A estrutura do multiprocessador \_ Caps \_ 1 é o formato para as informações de capacidade da impressora que são retornadas pela função GetPrinterData no buffer especificado pela variável pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Estrutura de PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796103"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="89452-103">Estrutura de Caps-PROCESSer \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="89452-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="89452-104">A estrutura do **multiprocessador \_ Caps \_ 1** é o formato para as informações de capacidade da impressora que são retornadas pela função [**GetPrinterData**](getprinterdata.md) no buffer especificado pela variável *pData* .</span><span class="sxs-lookup"><span data-stu-id="89452-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="89452-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89452-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="89452-106">Membros</span><span class="sxs-lookup"><span data-stu-id="89452-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="89452-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="89452-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="89452-108">O número de versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="89452-108">The structure's version number.</span></span> <span data-ttu-id="89452-109">Esse valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="89452-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="89452-110">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="89452-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="89452-111">Uma máscara de bits que representa os vários números de páginas de documentos que a impressora pode imprimir em uma página física.</span><span class="sxs-lookup"><span data-stu-id="89452-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="89452-112">O bit menos significativo representa 1 página de documento por página, o próximo bit representa 2 páginas de documento por página e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="89452-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="89452-113">Por exemplo, 0x0000810B indica que a impressora dá suporte a 1, 2, 4, 9 e 16 páginas de documento por página física.</span><span class="sxs-lookup"><span data-stu-id="89452-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="89452-114">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="89452-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="89452-115">A ordem na qual as páginas serão impressas.</span><span class="sxs-lookup"><span data-stu-id="89452-115">The order in which pages will be printed.</span></span> <span data-ttu-id="89452-116">Esse valor pode ser \_ impressão normal, impressão reversa \_ ou impressão de livretos \_ .</span><span class="sxs-lookup"><span data-stu-id="89452-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="89452-117">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="89452-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="89452-118">O número máximo de cópias que a impressora pode manipular.</span><span class="sxs-lookup"><span data-stu-id="89452-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89452-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="89452-119">Remarks</span></span>

<span data-ttu-id="89452-120">Os valores para todos os membros da estrutura são fornecidos pela função [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , que está documentada no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="89452-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="89452-121">O spooler chama uma função [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) do processador de impressão quando um aplicativo chama [**GetPrinterData**](getprinterdata.md), especificando um nome de valor com um formato de \_ *DataType* PrintProcCaps, em que *DataType* é o nome de um tipo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="89452-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="89452-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89452-122">Requirements</span></span>



| <span data-ttu-id="89452-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89452-123">Requirement</span></span> | <span data-ttu-id="89452-124">Valor</span><span class="sxs-lookup"><span data-stu-id="89452-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89452-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89452-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89452-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89452-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89452-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89452-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89452-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89452-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89452-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89452-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="89452-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89452-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89452-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="89452-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89452-132">Impressão</span><span class="sxs-lookup"><span data-stu-id="89452-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="89452-133">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="89452-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="89452-134">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="89452-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

