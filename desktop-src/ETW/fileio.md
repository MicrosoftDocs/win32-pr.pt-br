---
description: Essa classe é a classe pai para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Classe FileIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967725"
---
# <a name="fileio-class"></a><span data-ttu-id="57e3b-104">Classe FileIo</span><span class="sxs-lookup"><span data-stu-id="57e3b-104">FileIo class</span></span>

<span data-ttu-id="57e3b-105">Essa classe é a classe pai para eventos de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="57e3b-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="57e3b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e3b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57e3b-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="57e3b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="57e3b-108">Members</span></span>

<span data-ttu-id="57e3b-109">A classe **FileIo** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="57e3b-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="57e3b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="57e3b-110">Remarks</span></span>

<span data-ttu-id="57e3b-111">Para habilitar os eventos de e/s de arquivo em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ \_ e/s do arquivo de disco do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="57e3b-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="57e3b-112">Você também pode especificar um ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="57e3b-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="57e3b-113">**\_ \_ \_ e/s do arquivo de sinalizador de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="57e3b-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="57e3b-114">**\_inicialização de \_ es do arquivo de sinalizador de rastreamento de \_ \_ eventos \_**</span><span class="sxs-lookup"><span data-stu-id="57e3b-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="57e3b-115">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de arquivo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**FileIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="57e3b-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="57e3b-116">Use os tipos de evento a seguir para identificar o evento real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="57e3b-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="57e3b-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="57e3b-117">Event type</span></span>             | <span data-ttu-id="57e3b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="57e3b-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e3b-119">O valor do tipo de evento é 0</span><span class="sxs-lookup"><span data-stu-id="57e3b-119">Event type value is 0</span></span>  | <span data-ttu-id="57e3b-120">Evento de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-120">File name event.</span></span> <span data-ttu-id="57e3b-121">A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="57e3b-122">O valor do tipo de evento é 32</span><span class="sxs-lookup"><span data-stu-id="57e3b-122">Event type value is 32</span></span> | <span data-ttu-id="57e3b-123">Evento de criação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-123">File create event.</span></span> <span data-ttu-id="57e3b-124">A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="57e3b-125">O valor do tipo de evento é 35</span><span class="sxs-lookup"><span data-stu-id="57e3b-125">Event type value is 35</span></span> | <span data-ttu-id="57e3b-126">Evento de exclusão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-126">File delete event.</span></span> <span data-ttu-id="57e3b-127">A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="57e3b-128">O valor do tipo de evento é 36</span><span class="sxs-lookup"><span data-stu-id="57e3b-128">Event type value is 36</span></span> | <span data-ttu-id="57e3b-129">Evento de encerramento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-129">File rundown event.</span></span> <span data-ttu-id="57e3b-130">Enumera todos os arquivos abertos no computador no final da sessão de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="57e3b-131">A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="57e3b-132">O valor do tipo de evento é 64</span><span class="sxs-lookup"><span data-stu-id="57e3b-132">Event type value is 64</span></span> | <span data-ttu-id="57e3b-133">Evento de criação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-133">File create event.</span></span> <span data-ttu-id="57e3b-134">A classe [**FileIo \_ Create**](fileio-create.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="57e3b-135">O valor do tipo de evento é 72</span><span class="sxs-lookup"><span data-stu-id="57e3b-135">Event type value is 72</span></span> | <span data-ttu-id="57e3b-136">Evento de enumeração de diretório.</span><span class="sxs-lookup"><span data-stu-id="57e3b-136">Directory enumeration event.</span></span> <span data-ttu-id="57e3b-137">A [**classe \_ DirEnum**](fileio-direnum.md) do do FileIo é que define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="57e3b-138">O valor do tipo de evento é 77</span><span class="sxs-lookup"><span data-stu-id="57e3b-138">Event type value is 77</span></span> | <span data-ttu-id="57e3b-139">Evento de notificação de diretório.</span><span class="sxs-lookup"><span data-stu-id="57e3b-139">Directory notification event.</span></span> <span data-ttu-id="57e3b-140">A [**classe \_ DirEnum**](fileio-direnum.md) do do FileIo é que define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="57e3b-141">O valor do tipo de evento é 69</span><span class="sxs-lookup"><span data-stu-id="57e3b-141">Event type value is 69</span></span> | <span data-ttu-id="57e3b-142">Definir evento de informações.</span><span class="sxs-lookup"><span data-stu-id="57e3b-142">Set information event.</span></span> <span data-ttu-id="57e3b-143">A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="57e3b-144">O valor do tipo de evento é 70</span><span class="sxs-lookup"><span data-stu-id="57e3b-144">Event type value is 70</span></span> | <span data-ttu-id="57e3b-145">Excluir evento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-145">Delete file event.</span></span> <span data-ttu-id="57e3b-146">A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="57e3b-147">O valor do tipo de evento é 71</span><span class="sxs-lookup"><span data-stu-id="57e3b-147">Event type value is 71</span></span> | <span data-ttu-id="57e3b-148">Renomear o evento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-148">Rename file event.</span></span> <span data-ttu-id="57e3b-149">A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="57e3b-150">O valor do tipo de evento é 74</span><span class="sxs-lookup"><span data-stu-id="57e3b-150">Event type value is 74</span></span> | <span data-ttu-id="57e3b-151">Evento de informações do arquivo de consulta.</span><span class="sxs-lookup"><span data-stu-id="57e3b-151">Query file information event.</span></span> <span data-ttu-id="57e3b-152">A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="57e3b-153">O valor do tipo de evento é 75</span><span class="sxs-lookup"><span data-stu-id="57e3b-153">Event type value is 75</span></span> | <span data-ttu-id="57e3b-154">Evento de controle do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="57e3b-154">File system control event.</span></span> <span data-ttu-id="57e3b-155">A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="57e3b-156">O valor do tipo de evento é 76</span><span class="sxs-lookup"><span data-stu-id="57e3b-156">Event type value is 76</span></span> | <span data-ttu-id="57e3b-157">Fim do evento de operação.</span><span class="sxs-lookup"><span data-stu-id="57e3b-157">End of operation event.</span></span> <span data-ttu-id="57e3b-158">A classe MOF [**\_ aberta do FileIo**](fileio-opend.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="57e3b-159">O valor do tipo de evento é 67</span><span class="sxs-lookup"><span data-stu-id="57e3b-159">Event type value is 67</span></span> | <span data-ttu-id="57e3b-160">Evento de leitura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-160">File read event.</span></span> <span data-ttu-id="57e3b-161">A classe do MOF do [**FileIo \_ ReadWrite**](fileio-readwrite.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="57e3b-162">O valor do tipo de evento é 68</span><span class="sxs-lookup"><span data-stu-id="57e3b-162">Event type value is 68</span></span> | <span data-ttu-id="57e3b-163">Evento de gravação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="57e3b-163">File write event.</span></span> <span data-ttu-id="57e3b-164">A classe do MOF do [**FileIo \_ ReadWrite**](fileio-readwrite.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="57e3b-165">O valor do tipo de evento é 65</span><span class="sxs-lookup"><span data-stu-id="57e3b-165">Event type value is 65</span></span> | <span data-ttu-id="57e3b-166">Evento de limpeza.</span><span class="sxs-lookup"><span data-stu-id="57e3b-166">Clean up event.</span></span> <span data-ttu-id="57e3b-167">O evento é gerado quando o último identificador do arquivo é liberado.</span><span class="sxs-lookup"><span data-stu-id="57e3b-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="57e3b-168">A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="57e3b-169">O valor do tipo de evento é 66</span><span class="sxs-lookup"><span data-stu-id="57e3b-169">Event type value is 66</span></span> | <span data-ttu-id="57e3b-170">Fechar evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-170">Close event.</span></span> <span data-ttu-id="57e3b-171">O evento é gerado quando o objeto de arquivo é liberado.</span><span class="sxs-lookup"><span data-stu-id="57e3b-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="57e3b-172">A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="57e3b-173">O valor do tipo de evento é 73</span><span class="sxs-lookup"><span data-stu-id="57e3b-173">Event type value is 73</span></span> | <span data-ttu-id="57e3b-174">Evento de liberação.</span><span class="sxs-lookup"><span data-stu-id="57e3b-174">Flush event.</span></span> <span data-ttu-id="57e3b-175">Esse evento é gerado quando os buffers de arquivo são totalmente liberados para o disco.</span><span class="sxs-lookup"><span data-stu-id="57e3b-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="57e3b-176">A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="57e3b-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="57e3b-177">Os eventos de e/s de arquivo são registrados no início da operação.</span><span class="sxs-lookup"><span data-stu-id="57e3b-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e3b-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57e3b-178">Requirements</span></span>



| <span data-ttu-id="57e3b-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="57e3b-179">Requirement</span></span> | <span data-ttu-id="57e3b-180">Valor</span><span class="sxs-lookup"><span data-stu-id="57e3b-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57e3b-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57e3b-181">Minimum supported client</span></span><br/> | <span data-ttu-id="57e3b-182">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57e3b-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57e3b-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57e3b-183">Minimum supported server</span></span><br/> | <span data-ttu-id="57e3b-184">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57e3b-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57e3b-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="57e3b-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e3b-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="57e3b-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="57e3b-187">**\_V0 FileIo**</span><span class="sxs-lookup"><span data-stu-id="57e3b-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="57e3b-188">**FileIo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="57e3b-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
