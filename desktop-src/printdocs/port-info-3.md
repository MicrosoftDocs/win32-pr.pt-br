---
description: A \_ estrutura informações \_ de porta 3 especifica o valor de status de uma porta de impressora.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Estrutura de PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796155"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="39cec-103">Estrutura de informações da porta \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="39cec-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="39cec-104">A **estrutura \_ informações \_ de porta 3** especifica o valor de status de uma porta de impressora.</span><span class="sxs-lookup"><span data-stu-id="39cec-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="39cec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39cec-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="39cec-106">Membros</span><span class="sxs-lookup"><span data-stu-id="39cec-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="39cec-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="39cec-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="39cec-108">O novo valor de status da porta.</span><span class="sxs-lookup"><span data-stu-id="39cec-108">The new port status value.</span></span> <span data-ttu-id="39cec-109">Esse valor será usado somente se o membro **pszStatus** for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="39cec-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="39cec-110">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="39cec-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="39cec-111">Valor</span><span class="sxs-lookup"><span data-stu-id="39cec-111">Value</span></span>                            | <span data-ttu-id="39cec-112">Significado</span><span class="sxs-lookup"><span data-stu-id="39cec-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="39cec-113">0</span><span class="sxs-lookup"><span data-stu-id="39cec-113">0</span></span>                                | <span data-ttu-id="39cec-114">Limpa o status da porta da impressora.</span><span class="sxs-lookup"><span data-stu-id="39cec-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="39cec-115">STATUS da porta \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="39cec-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="39cec-116">A impressora da porta está offline.</span><span class="sxs-lookup"><span data-stu-id="39cec-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="39cec-117">\_ \_ emperramento de papel do status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="39cec-118">A impressora da porta tem um emperramento de papel.</span><span class="sxs-lookup"><span data-stu-id="39cec-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="39cec-119">\_saída do status da porta \_ \_</span><span class="sxs-lookup"><span data-stu-id="39cec-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="39cec-120">A impressora da porta está sem papel.</span><span class="sxs-lookup"><span data-stu-id="39cec-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="39cec-121">compartimento de saída de status da porta \_ \_ \_ \_ cheio</span><span class="sxs-lookup"><span data-stu-id="39cec-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="39cec-122">A bandeja de saída printer's da porta está cheia.</span><span class="sxs-lookup"><span data-stu-id="39cec-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="39cec-123">\_problema de \_ papel do status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="39cec-124">A impressora da porta tem um problema de papel.</span><span class="sxs-lookup"><span data-stu-id="39cec-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="39cec-125">STATUS da porta \_ \_ sem \_ toner</span><span class="sxs-lookup"><span data-stu-id="39cec-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="39cec-126">A impressora da porta está sem toner.</span><span class="sxs-lookup"><span data-stu-id="39cec-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="39cec-127">porta de status do porto \_ \_ \_ aberta</span><span class="sxs-lookup"><span data-stu-id="39cec-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="39cec-128">A porta da impressora da porta está aberta.</span><span class="sxs-lookup"><span data-stu-id="39cec-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="39cec-129">\_ \_ intervenção do usuário de status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="39cec-130">A impressora da porta requer intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="39cec-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="39cec-131">\_status \_ da porta fora \_ da \_ memória</span><span class="sxs-lookup"><span data-stu-id="39cec-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="39cec-132">A impressora da porta está sem memória.</span><span class="sxs-lookup"><span data-stu-id="39cec-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="39cec-133">\_toner de status de porta \_ \_ baixo</span><span class="sxs-lookup"><span data-stu-id="39cec-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="39cec-134">A impressora da porta está com pouco toner.</span><span class="sxs-lookup"><span data-stu-id="39cec-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="39cec-135">STATUS da porta \_ \_ aquecendo \_</span><span class="sxs-lookup"><span data-stu-id="39cec-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="39cec-136">A impressora da porta está se aquecendo.</span><span class="sxs-lookup"><span data-stu-id="39cec-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="39cec-137">\_economia de \_ energia de status de porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="39cec-138">A impressora da porta está em um modo de conservação de energia.</span><span class="sxs-lookup"><span data-stu-id="39cec-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="39cec-139">**pszStatus**</span><span class="sxs-lookup"><span data-stu-id="39cec-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="39cec-140">Ponteiro para uma nova cadeia de caracteres de valor de status de porta de impressora a ser definida.</span><span class="sxs-lookup"><span data-stu-id="39cec-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="39cec-141">Use esse membro se não houver nenhum valor de status adequado entre aqueles listados para **dwStatus**.</span><span class="sxs-lookup"><span data-stu-id="39cec-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="39cec-142">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="39cec-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="39cec-143">A severidade do valor de status da porta.</span><span class="sxs-lookup"><span data-stu-id="39cec-143">The severity of the port status value.</span></span>

<span data-ttu-id="39cec-144">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="39cec-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="39cec-145">Valor</span><span class="sxs-lookup"><span data-stu-id="39cec-145">Value</span></span>                       | <span data-ttu-id="39cec-146">Significado</span><span class="sxs-lookup"><span data-stu-id="39cec-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="39cec-147">\_erro de \_ tipo de status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="39cec-148">O valor de status da porta indica um erro.</span><span class="sxs-lookup"><span data-stu-id="39cec-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="39cec-149">\_aviso de \_ tipo de status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="39cec-150">O valor de status da porta é um aviso.</span><span class="sxs-lookup"><span data-stu-id="39cec-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="39cec-151">\_informações do \_ tipo de status da porta \_</span><span class="sxs-lookup"><span data-stu-id="39cec-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="39cec-152">O valor de status da porta é informativo.</span><span class="sxs-lookup"><span data-stu-id="39cec-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39cec-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="39cec-153">Remarks</span></span>

<span data-ttu-id="39cec-154">Quando você define um valor de status de porta de impressora com o valor de severidade \_ erro de tipo de status \_ \_ , o spooler de impressão para de enviar trabalhos para a porta.</span><span class="sxs-lookup"><span data-stu-id="39cec-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="39cec-155">O spooler de impressão não retoma o envio de trabalhos para a porta até que outra chamada [**SetPort**](setport.md) seja feita para limpar o status.</span><span class="sxs-lookup"><span data-stu-id="39cec-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="39cec-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39cec-156">Requirements</span></span>



| <span data-ttu-id="39cec-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="39cec-157">Requirement</span></span> | <span data-ttu-id="39cec-158">Valor</span><span class="sxs-lookup"><span data-stu-id="39cec-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39cec-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39cec-159">Minimum supported client</span></span><br/> | <span data-ttu-id="39cec-160">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39cec-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="39cec-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39cec-161">Minimum supported server</span></span><br/> | <span data-ttu-id="39cec-162">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39cec-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="39cec-163">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39cec-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="39cec-164"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39cec-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="39cec-165">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="39cec-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39cec-166">Informações de **\_ porta \_ \_ 3W** (Unicode) e **\_ informações de porta \_ \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="39cec-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="39cec-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="39cec-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cec-168">Impressão</span><span class="sxs-lookup"><span data-stu-id="39cec-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="39cec-169">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="39cec-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="39cec-170">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="39cec-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




