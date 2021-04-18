---
description: Representa informações de capacidade da impressora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Estrutura de PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763245"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="46f09-103">Estrutura do multiprocessador- \_ Caps \_ 2</span><span class="sxs-lookup"><span data-stu-id="46f09-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="46f09-104">Representa informações de capacidade da impressora.</span><span class="sxs-lookup"><span data-stu-id="46f09-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46f09-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="46f09-106">Membros</span><span class="sxs-lookup"><span data-stu-id="46f09-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46f09-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="46f09-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-108">Um valor que indica o número de versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="46f09-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="46f09-109">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="46f09-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-110">Uma máscara de bits que representa os vários números de páginas de documentos que a impressora pode imprimir em um único lado de uma folha física.</span><span class="sxs-lookup"><span data-stu-id="46f09-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="46f09-111">O bit menos significativo representa uma página de documento por lado, o próximo bit representa 2 páginas de documento por lado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="46f09-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="46f09-112">Por exemplo, 0x0000810B indica que a impressora dá suporte a 1, 2, 4, 9 e 16 páginas de documento por lado físico.</span><span class="sxs-lookup"><span data-stu-id="46f09-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="46f09-113">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="46f09-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-114">Um valor de sinalizador que indica a ordem em que as páginas serão impressas.</span><span class="sxs-lookup"><span data-stu-id="46f09-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="46f09-115">Pode ser impressão **normal \_**, **\_ impressão reversa** ou **\_ impressão de livretos**.</span><span class="sxs-lookup"><span data-stu-id="46f09-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="46f09-116">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="46f09-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-117">O número máximo de cópias que a impressora pode manipular.</span><span class="sxs-lookup"><span data-stu-id="46f09-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="46f09-118">**dwNupDirectionCaps**</span><span class="sxs-lookup"><span data-stu-id="46f09-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-119">Os padrões disponíveis quando várias páginas de documento são impressas no mesmo lado de uma folha de papel.</span><span class="sxs-lookup"><span data-stu-id="46f09-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="46f09-120">Os possíveis sinalizadores são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="46f09-120">The possible flags are the following:</span></span>



| <span data-ttu-id="46f09-121">Valor</span><span class="sxs-lookup"><span data-stu-id="46f09-121">Value</span></span>                     | <span data-ttu-id="46f09-122">Significado</span><span class="sxs-lookup"><span data-stu-id="46f09-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f09-123">PPCAPS \_ direita \_ e \_ abaixo</span><span class="sxs-lookup"><span data-stu-id="46f09-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="46f09-124">As páginas aparecem em linhas da direita para a esquerda, cada linha subsequente abaixo de sua predecessora.</span><span class="sxs-lookup"><span data-stu-id="46f09-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="46f09-125">PPCAPS \_ para baixo e para a \_ \_ direita</span><span class="sxs-lookup"><span data-stu-id="46f09-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="46f09-126">As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à direita de seu predecessor.</span><span class="sxs-lookup"><span data-stu-id="46f09-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="46f09-127">PPCAPS \_ à esquerda \_ e \_ para baixo</span><span class="sxs-lookup"><span data-stu-id="46f09-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="46f09-128">As páginas aparecem em linhas da esquerda para a direita, cada linha subsequente abaixo de sua predecessora.</span><span class="sxs-lookup"><span data-stu-id="46f09-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="46f09-129">PPCAPS \_ para baixo e para a \_ \_ esquerda</span><span class="sxs-lookup"><span data-stu-id="46f09-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="46f09-130">As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à esquerda de seu predecessor.</span><span class="sxs-lookup"><span data-stu-id="46f09-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="46f09-131">**dwNupBorderCaps**</span><span class="sxs-lookup"><span data-stu-id="46f09-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-132">Pode ser apenas PPCAPS \_ \_ a impressão de borda, indicando que, quando várias páginas de documento estão sendo impressas em um único lado de uma folha física, a impressora pode ser informada se deseja ou não imprimir uma borda em torno da área de imagem de cada página do documento.</span><span class="sxs-lookup"><span data-stu-id="46f09-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="46f09-133">**dwBookletHandlingCaps**</span><span class="sxs-lookup"><span data-stu-id="46f09-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-134">Só pode ser a \_ borda do livreto PPCAPS \_ , indicando que a impressora pode imprimir o estilo do livreto.</span><span class="sxs-lookup"><span data-stu-id="46f09-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="46f09-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="46f09-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="46f09-136">Valor</span><span class="sxs-lookup"><span data-stu-id="46f09-136">Value</span></span>                                         | <span data-ttu-id="46f09-137">Significado</span><span class="sxs-lookup"><span data-stu-id="46f09-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f09-138">PPCAPS \_ páginas inversas \_ \_ para \_ duplex reverso \_</span><span class="sxs-lookup"><span data-stu-id="46f09-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="46f09-139">Ao imprimir na ordem inversa e no duplex, o processador pode imprimir a ordem de cada par de páginas, portanto, em vez de imprimir na ordem 4, 3, 2, 1, eles serão impressos na ordem 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="46f09-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="46f09-140">PPCAPS \_ não \_ Enviar \_ \_ páginas extras \_ para \_ duplex</span><span class="sxs-lookup"><span data-stu-id="46f09-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="46f09-141">Ao duplex, o processador de impressão pode ser instruído a não enviar uma página extra quando há um número ímpar de páginas de documento.</span><span class="sxs-lookup"><span data-stu-id="46f09-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="46f09-142">O processador respeitará o valor da melhor maneira possível, mas nos casos em que a prevenção de uma página em branco extra poderia causar uma saída incorreta, as páginas extras ainda poderão ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="46f09-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="46f09-143">**dwScalingCaps**</span><span class="sxs-lookup"><span data-stu-id="46f09-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="46f09-144">Só pode ser PPCAPS \_ em \_ escala quadrada, indicando que a impressora pode dimensionar a imagem da página.</span><span class="sxs-lookup"><span data-stu-id="46f09-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46f09-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="46f09-145">Remarks</span></span>

<span data-ttu-id="46f09-146">Os valores para todos os membros da estrutura são fornecidos pela função **GetPrintProcessorCapabilities** , que está documentada no kit de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="46f09-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="46f09-147">Quando um aplicativo chama [**GetPrinterData**](getprinterdata.md), o spooler chama uma função **GetPrintProcessorCapabilities** do processador de impressão e especifica um nome de valor que tem um formato de _DataType_ **PrintProcCaps \_**, em que *DataType* é o nome de um tipo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="46f09-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="46f09-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f09-148">Requirements</span></span>



| <span data-ttu-id="46f09-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f09-149">Requirement</span></span> | <span data-ttu-id="46f09-150">Valor</span><span class="sxs-lookup"><span data-stu-id="46f09-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f09-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46f09-151">Minimum supported client</span></span><br/> | <span data-ttu-id="46f09-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46f09-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="46f09-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46f09-153">Minimum supported server</span></span><br/> | <span data-ttu-id="46f09-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46f09-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46f09-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46f09-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f09-156"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46f09-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f09-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="46f09-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f09-158">Impressão</span><span class="sxs-lookup"><span data-stu-id="46f09-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="46f09-159">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="46f09-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="46f09-160">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="46f09-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




