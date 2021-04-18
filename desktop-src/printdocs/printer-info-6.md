---
description: As informações da impressora \_ \_ 6 especificam o valor de status de uma impressora.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Estrutura de PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771362"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="85cf8-103">Estrutura de informações da impressora \_ \_ 6</span><span class="sxs-lookup"><span data-stu-id="85cf8-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="85cf8-104">As **informações da impressora \_ \_ 6** especificam o valor de status de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="85cf8-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cf8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85cf8-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="85cf8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="85cf8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="85cf8-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="85cf8-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="85cf8-108">O status da impressora.</span><span class="sxs-lookup"><span data-stu-id="85cf8-108">The printer status.</span></span> <span data-ttu-id="85cf8-109">Esse membro pode ser qualquer combinação razoável dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="85cf8-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="85cf8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="85cf8-110">Value</span></span>                               | <span data-ttu-id="85cf8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="85cf8-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cf8-112">STATUS da impressora \_ \_ ocupado</span><span class="sxs-lookup"><span data-stu-id="85cf8-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="85cf8-113">A impressora está ocupada.</span><span class="sxs-lookup"><span data-stu-id="85cf8-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="85cf8-114">porta de status da impressora \_ \_ \_ aberta</span><span class="sxs-lookup"><span data-stu-id="85cf8-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="85cf8-115">A porta da impressora está aberta.</span><span class="sxs-lookup"><span data-stu-id="85cf8-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="85cf8-116">\_erro de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="85cf8-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="85cf8-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="85cf8-118">\_inicialização do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="85cf8-119">A impressora está sendo inicializada.</span><span class="sxs-lookup"><span data-stu-id="85cf8-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="85cf8-120">STATUS da impressora \_ \_ e/s \_ ativa</span><span class="sxs-lookup"><span data-stu-id="85cf8-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="85cf8-121">A impressora está em um estado de entrada/saída ativo</span><span class="sxs-lookup"><span data-stu-id="85cf8-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="85cf8-122">\_ \_ feed manual de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="85cf8-123">A impressora está em um estado de feed manual.</span><span class="sxs-lookup"><span data-stu-id="85cf8-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="85cf8-124">STATUS da impressora \_ \_ sem \_ toner</span><span class="sxs-lookup"><span data-stu-id="85cf8-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="85cf8-125">A impressora está sem toner.</span><span class="sxs-lookup"><span data-stu-id="85cf8-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="85cf8-126">STATUS da impressora \_ \_ não \_ disponível</span><span class="sxs-lookup"><span data-stu-id="85cf8-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="85cf8-127">A impressora não está disponível para impressão.</span><span class="sxs-lookup"><span data-stu-id="85cf8-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="85cf8-128">STATUS da impressora \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="85cf8-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="85cf8-129">A impressora está offline.</span><span class="sxs-lookup"><span data-stu-id="85cf8-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="85cf8-130">\_status \_ da impressora fora \_ da \_ memória</span><span class="sxs-lookup"><span data-stu-id="85cf8-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="85cf8-131">A impressora ficou sem memória.</span><span class="sxs-lookup"><span data-stu-id="85cf8-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="85cf8-132">bandeja de saída de status da impressora \_ \_ \_ \_ cheia</span><span class="sxs-lookup"><span data-stu-id="85cf8-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="85cf8-133">O compartimento de saída da impressora está cheio.</span><span class="sxs-lookup"><span data-stu-id="85cf8-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="85cf8-134">\_ \_ apontador de página de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="85cf8-135">A impressora não pode imprimir a página atual.</span><span class="sxs-lookup"><span data-stu-id="85cf8-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="85cf8-136">\_ \_ emperramento de papel do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="85cf8-137">O papel está emperrado na impressora</span><span class="sxs-lookup"><span data-stu-id="85cf8-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="85cf8-138">\_saída do status da impressora \_ \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="85cf8-139">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="85cf8-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="85cf8-140">\_problema de \_ papel do status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="85cf8-141">A impressora tem um problema de papel.</span><span class="sxs-lookup"><span data-stu-id="85cf8-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="85cf8-142">STATUS da impressora em \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="85cf8-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="85cf8-143">A impressora está em pausa.</span><span class="sxs-lookup"><span data-stu-id="85cf8-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="85cf8-144">\_exclusão de status \_ da impressora pendente \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="85cf8-145">A exclusão da impressora está pendente como resultado de uma chamada para a função [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="85cf8-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="85cf8-146">\_economia de \_ energia de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="85cf8-147">A impressora está no modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="85cf8-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="85cf8-148">\_impressão de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="85cf8-149">A impressora está imprimindo.</span><span class="sxs-lookup"><span data-stu-id="85cf8-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="85cf8-150">\_processamento de status da impressora \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="85cf8-151">A impressora está processando um comando da função [**Setprinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="85cf8-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="85cf8-152">servidor de status de impressora \_ \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="85cf8-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="85cf8-153">O status da impressora é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="85cf8-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="85cf8-154">\_toner de status da impressora \_ \_ baixo</span><span class="sxs-lookup"><span data-stu-id="85cf8-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="85cf8-155">A impressora está com pouco toner.</span><span class="sxs-lookup"><span data-stu-id="85cf8-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="85cf8-156">\_status da \_ impressora \_ intervenção do usuário</span><span class="sxs-lookup"><span data-stu-id="85cf8-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="85cf8-157">A impressora tem um erro que exige que o usuário faça algo.</span><span class="sxs-lookup"><span data-stu-id="85cf8-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="85cf8-158">STATUS da impressora \_ \_ aguardando</span><span class="sxs-lookup"><span data-stu-id="85cf8-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="85cf8-159">A impressora está aguardando.</span><span class="sxs-lookup"><span data-stu-id="85cf8-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="85cf8-160">STATUS da impressora \_ \_ aquecendo \_</span><span class="sxs-lookup"><span data-stu-id="85cf8-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="85cf8-161">A impressora está em preparação.</span><span class="sxs-lookup"><span data-stu-id="85cf8-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85cf8-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85cf8-162">Requirements</span></span>



| <span data-ttu-id="85cf8-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cf8-163">Requirement</span></span> | <span data-ttu-id="85cf8-164">Valor</span><span class="sxs-lookup"><span data-stu-id="85cf8-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cf8-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85cf8-165">Minimum supported client</span></span><br/> | <span data-ttu-id="85cf8-166">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="85cf8-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85cf8-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85cf8-167">Minimum supported server</span></span><br/> | <span data-ttu-id="85cf8-168">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="85cf8-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85cf8-169">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="85cf8-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="85cf8-170"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85cf8-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="85cf8-171">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="85cf8-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85cf8-172">**\_ Informações de impressora \_ \_ 6W** (Unicode) e **\_ info de impressora \_ \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85cf8-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="85cf8-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="85cf8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cf8-174">Impressão</span><span class="sxs-lookup"><span data-stu-id="85cf8-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="85cf8-175">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="85cf8-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="85cf8-176">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="85cf8-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="85cf8-177">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="85cf8-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="85cf8-178">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="85cf8-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="85cf8-179">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="85cf8-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="85cf8-180">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="85cf8-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="85cf8-181">**Informações da impressora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="85cf8-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




