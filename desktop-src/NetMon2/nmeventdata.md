---
description: A estrutura NMEVENTDATA contém informações sobre uma condição de evento que é passada para Monitor de Rede para inserir uma linha no Visualizador de especialistas.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estrutura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827345"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="807e8-103">Estrutura NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="807e8-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="807e8-104">A estrutura **NMEVENTDATA** contém informações sobre uma condição de evento que é passada para monitor de rede para inserir uma linha no Visualizador de especialistas.</span><span class="sxs-lookup"><span data-stu-id="807e8-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="807e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="807e8-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="807e8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="807e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="807e8-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="807e8-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-108">Número de versão da estrutura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="807e8-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="807e8-109">O número de versão deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="807e8-109">The version number must be zero.</span></span> <span data-ttu-id="807e8-110">Versões futuras do Monitor de Rede podem dar suporte a um número de versão mais alto.</span><span class="sxs-lookup"><span data-stu-id="807e8-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-111">**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="807e8-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-112">Identificador do evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-112">Identifier of the event.</span></span> <span data-ttu-id="807e8-113">**EventIdent** é exclusivo para cada especialista e faz referência a uma [página de referência de evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="807e8-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="807e8-114">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="807e8-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-115">Um conjunto de sinalizadores que descreve quem envia os dados do evento e como o evento é exibido.</span><span class="sxs-lookup"><span data-stu-id="807e8-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="807e8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="807e8-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="807e8-117">Significado</span><span class="sxs-lookup"><span data-stu-id="807e8-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="807e8-118"><dt>**\_especialista em sinalizador de eventos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="807e8-119">O evento provém de um especialista.</span><span class="sxs-lookup"><span data-stu-id="807e8-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="807e8-120"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ severidade**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="807e8-121">Não exiba o nível de severidade do evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="807e8-122"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ origem**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="807e8-123">Não exiba o nome de origem do evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="807e8-124"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ nome do evento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="807e8-125">Não exiba o nome do evento para o evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="807e8-126"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ Descrição**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="807e8-127">Não exiba a descrição do evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="807e8-128"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ computador**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="807e8-129">Não exiba o nome do computador para o evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="807e8-130"><dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ hora**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="807e8-131">Não exibir a hora do evento</span><span class="sxs-lookup"><span data-stu-id="807e8-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="807e8-132"><dt>**NMEVENTFLAG \_ \_ não \_ exibem \_ colunas fixas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="807e8-133">Não exiba as colunas gravidade, origem, nome do evento, descrição, máquina ou hora.</span><span class="sxs-lookup"><span data-stu-id="807e8-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="807e8-134">Isso não é um sinalizador único, mas é uma União dos seis sinalizadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="807e8-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="807e8-135">**Gravidade**</span><span class="sxs-lookup"><span data-stu-id="807e8-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-136">Nível de severidade do evento.</span><span class="sxs-lookup"><span data-stu-id="807e8-136">Severity level of the event.</span></span> <span data-ttu-id="807e8-137">O nível de severidade pode ter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="807e8-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="807e8-138">NMEVENT \_ severidade \_ informativa NMEVENT aviso de severidade \_ \_ NMEVENT \_ severidade \_ forte \_ aviso NMEVENT erro de severidade \_ \_ NMEVENT \_ gravidade \_ grave \_ erro NMEVENT \_ gravidade \_ crítica \_ erro</span><span class="sxs-lookup"><span data-stu-id="807e8-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="807e8-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="807e8-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-140">Número de colunas designadas na estrutura atual.</span><span class="sxs-lookup"><span data-stu-id="807e8-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-141">**szSourceName**</span><span class="sxs-lookup"><span data-stu-id="807e8-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-142">Nome do especialista exibido.</span><span class="sxs-lookup"><span data-stu-id="807e8-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-143">**szEventName**</span><span class="sxs-lookup"><span data-stu-id="807e8-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-144">Nome do evento que é exibido.</span><span class="sxs-lookup"><span data-stu-id="807e8-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="807e8-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-146">Descrição do evento que é exibido.</span><span class="sxs-lookup"><span data-stu-id="807e8-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-147">**szMachine**</span><span class="sxs-lookup"><span data-stu-id="807e8-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-148">Obsoleto, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="807e8-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-149">**Justificativa**</span><span class="sxs-lookup"><span data-stu-id="807e8-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-150">Informações exibidas na segunda janela do Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="807e8-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="807e8-151">O membro de **justificativa** pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="807e8-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="807e8-152">Se for **NULL**, a segunda janela não estará visível.</span><span class="sxs-lookup"><span data-stu-id="807e8-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-153">**szUrl**</span><span class="sxs-lookup"><span data-stu-id="807e8-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-154">Reservado Este membro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="807e8-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="807e8-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-156">Hora em que a condição de evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="807e8-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="807e8-157">O tempo é medido em relação ao início da captura.</span><span class="sxs-lookup"><span data-stu-id="807e8-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="807e8-158">**Coluna**</span><span class="sxs-lookup"><span data-stu-id="807e8-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="807e8-159">Tabela de estruturas de coluna que aparece no painel superior da Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="807e8-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="807e8-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="807e8-160">Requirements</span></span>



| <span data-ttu-id="807e8-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="807e8-161">Requirement</span></span> | <span data-ttu-id="807e8-162">Valor</span><span class="sxs-lookup"><span data-stu-id="807e8-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="807e8-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="807e8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="807e8-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="807e8-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="807e8-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="807e8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="807e8-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="807e8-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="807e8-167">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="807e8-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="807e8-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="807e8-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




