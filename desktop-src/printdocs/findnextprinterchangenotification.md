---
description: A função FindNextPrinterChangeNotification recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a um servidor de impressão ou impressora.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Função FindNextPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828920"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="63e89-103">Função FindNextPrinterChangeNotification</span><span class="sxs-lookup"><span data-stu-id="63e89-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="63e89-104">A função **FindNextPrinterChangeNotification** recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a um servidor de impressão ou impressora.</span><span class="sxs-lookup"><span data-stu-id="63e89-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="63e89-105">Chame essa função quando uma operação de espera no objeto de notificação de alteração for satisfeita.</span><span class="sxs-lookup"><span data-stu-id="63e89-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="63e89-106">A função também redefine o objeto de notificação de alteração para o estado não sinalizado.</span><span class="sxs-lookup"><span data-stu-id="63e89-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="63e89-107">Você pode usar o objeto em outra operação de espera para continuar a monitorar a impressora ou o servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="63e89-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="63e89-108">O sistema operacional definirá o objeto para o estado sinalizado na próxima vez que um de um conjunto especificado de alterações ocorrer na impressora ou no servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="63e89-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="63e89-109">A função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) cria o objeto de notificação de alteração e especifica o conjunto de alterações a ser monitorado.</span><span class="sxs-lookup"><span data-stu-id="63e89-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e89-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63e89-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="63e89-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63e89-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e89-112">*hChange* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63e89-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e89-113">Um identificador para um objeto de notificação de alteração associado a uma impressora ou a um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="63e89-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="63e89-114">Você obtém esse identificador chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="63e89-115">O sistema operacional define esse objeto de notificação de alteração para o estado sinalizado quando detecta uma das alterações especificadas no filtro de notificação de alteração do objeto.</span><span class="sxs-lookup"><span data-stu-id="63e89-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="63e89-116">*pdwChange* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63e89-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63e89-117">Um ponteiro para uma variável cujos bits são definidos para indicar as alterações que ocorreram para causar a notificação mais recente.</span><span class="sxs-lookup"><span data-stu-id="63e89-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="63e89-118">Os sinalizadores de bit que podem ser definidos correspondem àqueles especificados no parâmetro *fdwFilter* da chamada [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="63e89-119">O sistema define um ou mais dos seguintes sinalizadores de bits.</span><span class="sxs-lookup"><span data-stu-id="63e89-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="63e89-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63e89-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="63e89-121">Significado</span><span class="sxs-lookup"><span data-stu-id="63e89-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="63e89-122"><dt>**\_ \_ Adicionar formulário de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="63e89-123">Um formulário foi adicionado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="63e89-124"><dt>**\_ \_ Adicionar trabalho de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="63e89-125">Um trabalho de impressão foi enviado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="63e89-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="63e89-126"><dt>**\_ \_ Adicionar porta alterar \_ impressora**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="63e89-127">Uma porta ou monitor foi adicionado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="63e89-128"><dt>**mudança de impressora \_ \_ Adicionar \_ processador de impressão \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="63e89-129">Um processador de impressão foi adicionado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="63e89-130"><dt>**\_ \_ Adicionar impressora alterar \_ impressora**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="63e89-131">Uma impressora foi adicionada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="63e89-132"><dt>**\_alterar impressora \_ Adicionar \_ Driver de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="63e89-133">Um driver de impressora foi adicionado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="63e89-134"><dt>**\_porta de \_ configuração de alteração da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="63e89-135">Uma porta foi configurada no servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="63e89-136"><dt>**\_formulário de \_ exclusão de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="63e89-137">Um formulário foi excluído do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="63e89-138"><dt>**\_trabalho de \_ exclusão de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="63e89-139">Um trabalho foi excluído.</span><span class="sxs-lookup"><span data-stu-id="63e89-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="63e89-140"><dt>**\_porta de \_ exclusão de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="63e89-141">Uma porta ou monitor foi excluído do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="63e89-142"><dt>**\_processador de \_ exclusão de alteração \_ de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="63e89-143">Um processador de impressão foi excluído do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="63e89-144"><dt>**impressora de \_ exclusão de alteração de impressora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="63e89-145">Uma impressora foi excluída.</span><span class="sxs-lookup"><span data-stu-id="63e89-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="63e89-146"><dt>**\_Driver de \_ impressora de exclusão de alteração de impressora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="63e89-147">Um driver de impressora foi excluído do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="63e89-148"><dt>**impressora de conexão de alteração de impressora \_ \_ com falha \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="63e89-149">Falha em uma conexão de impressora.</span><span class="sxs-lookup"><span data-stu-id="63e89-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="63e89-150"><dt>**\_formulário do \_ conjunto de alterações da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="63e89-151">Um formulário foi definido no servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="63e89-152"><dt>**\_trabalho do \_ conjunto de alterações da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="63e89-153">Um trabalho foi definido.</span><span class="sxs-lookup"><span data-stu-id="63e89-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="63e89-154"><dt>**\_impressora do \_ conjunto de alterações da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="63e89-155">Uma impressora foi definida.</span><span class="sxs-lookup"><span data-stu-id="63e89-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="63e89-156"><dt>**\_Driver de \_ impressora do conjunto de alterações de impressora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="63e89-157">Um driver de impressora foi definido.</span><span class="sxs-lookup"><span data-stu-id="63e89-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="63e89-158"><dt>**\_trabalho de \_ gravação de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="63e89-159">Os dados do trabalho foram gravados.</span><span class="sxs-lookup"><span data-stu-id="63e89-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="63e89-160"><dt>**\_tempo limite de alteração da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="63e89-161">O tempo limite do trabalho foi atingido.</span><span class="sxs-lookup"><span data-stu-id="63e89-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="63e89-162"><dt>**\_servidor de alteração de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="63e89-163">Windows 7: ocorreu uma alteração no servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="63e89-164">*pPrinterNotifyOptions* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63e89-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63e89-165">Um ponteiro para uma estrutura de [**\_ \_ Opções de notificação de impressora**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="63e89-166">Defina o membro **flags** desta estrutura para **Opções de \_ notificação de impressora \_ \_ Atualizar**, para fazer com que a função retorne os dados atuais para todos os campos de informações de impressora monitorados.</span><span class="sxs-lookup"><span data-stu-id="63e89-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="63e89-167">A função ignora todos os outros membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="63e89-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="63e89-168">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="63e89-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="63e89-169">*ppPrinterNotifyInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63e89-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63e89-170">Um ponteiro para uma variável de ponteiro que recebe um ponteiro para um buffer somente leitura alocado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="63e89-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="63e89-171">Chame a função [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar o buffer quando tiver terminado de fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="63e89-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="63e89-172">Esse parâmetro poderá ser **nulo** se nenhuma informação for necessária.</span><span class="sxs-lookup"><span data-stu-id="63e89-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="63e89-173">O buffer contém uma estrutura de [**\_ \_ informações de notificação de impressora**](printer-notify-info.md) , que contém uma matriz de estruturas de [**\_ \_ \_ dados de informações de notificação de impressora**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="63e89-174">Cada elemento da matriz contém informações sobre um dos campos especificados no parâmetro *pPrinterNotifyOptions* da chamada [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="63e89-175">Normalmente, a função fornece dados somente para os campos que foram alterados para causar a notificação mais recente.</span><span class="sxs-lookup"><span data-stu-id="63e89-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="63e89-176">No entanto, se a estrutura apontada pelo parâmetro *pPrinterNotifyOptions* especificar **Opções de notificação de impressora \_ \_ \_ Atualizar**, a função fornecerá dados para todos os campos monitorados.</span><span class="sxs-lookup"><span data-stu-id="63e89-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="63e89-177">Se o bit de **notificação de informação de impressora \_ \_ \_ descartada** estiver definido no membro **flags** da estrutura de [**\_ \_ informações de notificação da impressora**](printer-notify-info.md) , ocorrerá um estouro ou erro e as notificações podem ter sido perdidas.</span><span class="sxs-lookup"><span data-stu-id="63e89-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="63e89-178">Nesse caso, nenhuma notificação adicional será enviada até que você faça uma segunda chamada **FindNextPrinterChangeNotification** que especifica a **\_ atualização das \_ opções \_ de notificação de impressora**.</span><span class="sxs-lookup"><span data-stu-id="63e89-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e89-179">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63e89-179">Return value</span></span>

<span data-ttu-id="63e89-180">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="63e89-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="63e89-181">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="63e89-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e89-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="63e89-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63e89-183">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="63e89-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="63e89-184">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63e89-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="63e89-185">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="63e89-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="63e89-186">Chame a função **FindNextPrinterChangeNotification** depois que uma operação de espera em um objeto de notificação criado por [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) tiver sido satisfeita.</span><span class="sxs-lookup"><span data-stu-id="63e89-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="63e89-187">Chamar **FindNextPrinterChangeNotification** permite que você obtenha informações sobre a alteração que satisfez a operação de espera e redefine o objeto de notificação para que ele possa ser sinalizado quando ocorrer a próxima alteração.</span><span class="sxs-lookup"><span data-stu-id="63e89-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="63e89-188">Com uma exceção, não chame a função **FindNextPrinterChangeNotification** se o objeto de notificação de alteração não estiver no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="63e89-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="63e89-189">Se uma função Wait retornar o **\_ tempo limite de espera** de valor, o objeto de alteração não estará no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="63e89-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="63e89-190">Chame a função **FindNextPrinterChangeNotification** somente se a função Wait for realizada com sucesso sem tempo limite. A exceção é quando **FindNextPrinterChangeNotification** é chamado com o bit de **\_ \_ \_ atualização opções de notificação de impressora** definido no parâmetro *pPrinterNotifyOptions* .</span><span class="sxs-lookup"><span data-stu-id="63e89-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="63e89-191">Observe que mesmo quando esse sinalizador é definido, ainda é possível que o sinalizador **de \_ \_ informações de \_ notificação de impressora** seja definido no parâmetro *ppPrinterNotifyInfo* .</span><span class="sxs-lookup"><span data-stu-id="63e89-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="63e89-192">Para continuar a monitorar as alterações na impressora ou no servidor de impressão, repita o ciclo de chamar uma das [funções de espera](/windows/desktop/Sync/wait-functions) e, em seguida, chamando a função **FindNextPrinterChangeNotification** para examinar a alteração e redefinir o objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="63e89-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="63e89-193">**FindNextPrinterChangeNotification** pode combinar várias alterações no mesmo campo de informações de impressora em uma única notificação.</span><span class="sxs-lookup"><span data-stu-id="63e89-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="63e89-194">Quando isso ocorre, a função normalmente recolhe todas as alterações do campo em uma única entrada na matriz de estruturas de [**\_ dados de \_ informações \_ de notificação de impressora**](printer-notify-info-data.md) em *ppPrinterNotifyInfo*; a única entrada relata apenas as informações mais atuais.</span><span class="sxs-lookup"><span data-stu-id="63e89-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="63e89-195">No entanto, para alguns campos de informações de trabalho e impressora, a função pode retornar várias entradas de matriz para o mesmo campo.</span><span class="sxs-lookup"><span data-stu-id="63e89-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="63e89-196">Nesse caso, a última entrada de matriz para o campo relata os dados atuais e as entradas anteriores contêm os dados para os estágios intermediários.</span><span class="sxs-lookup"><span data-stu-id="63e89-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="63e89-197">Quando você não precisar mais do objeto de notificação de alteração, feche-o chamando a função [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="63e89-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="63e89-198">No Windows XP com Service Pack 2 (SP2) e posterior, o firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras pode ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="63e89-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="63e89-199">Se um usuário fizer uma conexão de impressora com outro computador e a exceção não estiver habilitada, o usuário não receberá notificações de alteração de impressora do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e89-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="63e89-200">Um administrador de máquina precisará habilitar a exceção.</span><span class="sxs-lookup"><span data-stu-id="63e89-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="63e89-201">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63e89-201">Examples</span></span>

<span data-ttu-id="63e89-202">O exemplo de código a seguir ilustra como você pode monitorar o status da impressora usando essas funções.</span><span class="sxs-lookup"><span data-stu-id="63e89-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="63e89-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e89-203">Requirements</span></span>



| <span data-ttu-id="63e89-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e89-204">Requirement</span></span> | <span data-ttu-id="63e89-205">Valor</span><span class="sxs-lookup"><span data-stu-id="63e89-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e89-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63e89-206">Minimum supported client</span></span><br/> | <span data-ttu-id="63e89-207">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63e89-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63e89-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63e89-208">Minimum supported server</span></span><br/> | <span data-ttu-id="63e89-209">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63e89-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63e89-210">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63e89-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e89-211"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="63e89-212">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63e89-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="63e89-213"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="63e89-214">DLL</span><span class="sxs-lookup"><span data-stu-id="63e89-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e89-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e89-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="63e89-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="63e89-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e89-217">Impressão</span><span class="sxs-lookup"><span data-stu-id="63e89-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="63e89-218">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="63e89-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="63e89-219">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="63e89-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="63e89-220">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="63e89-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="63e89-221">**\_informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="63e89-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="63e89-222">**\_dados de \_ informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="63e89-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="63e89-223">**\_Opções de notificação de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="63e89-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

