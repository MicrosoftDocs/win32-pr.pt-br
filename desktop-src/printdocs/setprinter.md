---
description: A função setprinter define os dados de uma impressora especificada ou define o estado da impressora especificada pausando a impressão, retomando a impressão ou limpando todos os trabalhos de impressão.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Função setprinter (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764213"
---
# <a name="setprinter-function"></a><span data-ttu-id="31ac1-103">Função setprinter</span><span class="sxs-lookup"><span data-stu-id="31ac1-103">SetPrinter function</span></span>

<span data-ttu-id="31ac1-104">A função **Setprinter** define os dados de uma impressora especificada ou define o estado da impressora especificada pausando a impressão, retomando a impressão ou limpando todos os trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="31ac1-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ac1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31ac1-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="31ac1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ac1-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ac1-108">Um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-108">A handle to the printer.</span></span> <span data-ttu-id="31ac1-109">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="31ac1-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ac1-111">O tipo de dados que a função armazena no buffer apontado por *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="31ac1-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="31ac1-112">Se o parâmetro de *comando* não for igual a zero, o parâmetro *Level* deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="31ac1-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="31ac1-113">Esse valor pode ser 0, 2, 3, 4, 5, 6, 7, 8 ou 9.</span><span class="sxs-lookup"><span data-stu-id="31ac1-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="31ac1-114">*pPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ac1-115">Um ponteiro para um buffer que contém dados a serem definidos para a impressora ou que contêm informações para o comando especificado pelo parâmetro de *comando* .</span><span class="sxs-lookup"><span data-stu-id="31ac1-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="31ac1-116">O tipo de dados no buffer é determinado pelo valor do *nível*.</span><span class="sxs-lookup"><span data-stu-id="31ac1-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="31ac1-117">Nível</span><span class="sxs-lookup"><span data-stu-id="31ac1-117">Level</span></span>                                                                                                | <span data-ttu-id="31ac1-118">Estrutura</span><span class="sxs-lookup"><span data-stu-id="31ac1-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="31ac1-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="31ac1-120">Se o parâmetro de *comando* for **Printer \_ Control \_ set \_ status**, *pPrinter* deverá conter um valor **DWORD** que especifica o novo status da impressora a ser definido.</span><span class="sxs-lookup"><span data-stu-id="31ac1-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="31ac1-121">Para obter uma lista dos possíveis valores de status, consulte o membro **status** da [**estrutura \_ info \_ 2 da impressora**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="31ac1-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="31ac1-122">Observe que o **status da impressora em \_ \_ pausa** e a **\_ exclusão do status da impressora \_ pendente \_** não são valores de status válidos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="31ac1-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="31ac1-123">Se o *nível* for 0, mas o parâmetro de *comando* não for um status de  **conjunto de controle de impressora \_ \_ \_**, pPrinter deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="31ac1-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="31ac1-125">Uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações detalhadas sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="31ac1-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="31ac1-127">Uma estrutura de [**informações da impressora \_ \_ 3**](printer-info-3.md) que contém as informações de segurança da impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="31ac1-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="31ac1-129">Uma estrutura de [**informações da impressora \_ \_ 4**](printer-info-4.md) que contém informações de impressora mínimas, incluindo o nome da impressora, o nome do servidor e se a impressora é remota ou local.</span><span class="sxs-lookup"><span data-stu-id="31ac1-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="31ac1-130"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="31ac1-131">Uma estrutura de [**informações da impressora \_ \_ 5**](printer-info-5.md) que contém informações de impressora, como atributos de impressora e configurações de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="31ac1-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="31ac1-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="31ac1-133">Uma estrutura de [**informações da impressora \_ \_ 6**](printer-info-6.md) especificando o valor de status de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="31ac1-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="31ac1-135">Uma estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) .</span><span class="sxs-lookup"><span data-stu-id="31ac1-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="31ac1-136">O membro *dwAction* dessa estrutura indica se o **setimprimíer** deve publicar, cancelar a publicação, publicar novamente ou atualizar os dados da impressora no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="31ac1-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="31ac1-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="31ac1-138">Uma estrutura de [**informações da impressora \_ \_ 8**](printer-info-8.md) especificando as configurações de impressora padrão globais.</span><span class="sxs-lookup"><span data-stu-id="31ac1-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="31ac1-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="31ac1-140">Uma estrutura de [**informações da impressora \_ \_ 9**](printer-info-9.md) especificando as configurações de impressora padrão por usuário.</span><span class="sxs-lookup"><span data-stu-id="31ac1-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="31ac1-141">*Comando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ac1-142">a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-142">The action to perform.</span></span>

<span data-ttu-id="31ac1-143">Se o parâmetro de *nível* for diferente de zero, defina o valor desse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="31ac1-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="31ac1-144">Nesse caso, a impressora retém seu estado atual e a função reconfigura os dados da impressora conforme especificado pelos parâmetros *Level* e *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="31ac1-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="31ac1-145">Se o parâmetro *Level* for zero, defina o valor desse parâmetro como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="31ac1-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="31ac1-146">Valor</span><span class="sxs-lookup"><span data-stu-id="31ac1-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="31ac1-147">Significado</span><span class="sxs-lookup"><span data-stu-id="31ac1-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="31ac1-148"><dt>**\_pausa de controle de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="31ac1-149">Pausar a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="31ac1-150"><dt>**\_limpeza de controle de impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="31ac1-151">Exclua todos os trabalhos de impressão na impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="31ac1-152"><dt>**retomada de controle de impressora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="31ac1-153">Retomar uma impressora pausada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="31ac1-154"><dt>**\_status do \_ conjunto de controle da impressora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="31ac1-155">Defina o status da impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-155">Set the printer status.</span></span><br/> <span data-ttu-id="31ac1-156">Defina o parâmetro *pPrinter* como um ponteiro para um valor **DWORD** que especifica o novo status da impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ac1-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31ac1-157">Return value</span></span>

<span data-ttu-id="31ac1-158">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="31ac1-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="31ac1-159">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="31ac1-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="31ac1-160">Se o *nível* for 7 e a ação de publicação falhar, **setprinter** retornará uma **\_ e/s de erro \_ pendente** e tentará concluir a ação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="31ac1-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="31ac1-161">Se o *nível* for 7 e a ação de atualização falhar, o **setprinter** retornará o **arquivo de erro \_ \_ não \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ac1-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="31ac1-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31ac1-163">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="31ac1-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="31ac1-164">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31ac1-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="31ac1-165">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="31ac1-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="31ac1-166">Não é possível usar **Setprinter** para alterar a impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="31ac1-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="31ac1-167">Para modificar as configurações atuais da impressora, chame a função [**Getprinter**](getprinter.md) para recuperar as configurações atuais em uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) , modifique os membros dessa estrutura conforme necessário e, em seguida, chame **setprinter**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="31ac1-168">A função **Setprinter** ignora os membros **pServerName**, **AveragePPM**, **status** e **cJobs** de uma estrutura de [**informações de impressora \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="31ac1-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="31ac1-169">Pausar uma impressora suspende o agendamento de todos os trabalhos de impressão para essa impressora, exceto para um trabalho de impressão que pode estar sendo impresso no momento.</span><span class="sxs-lookup"><span data-stu-id="31ac1-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="31ac1-170">Os trabalhos de impressão podem ser enviados para uma impressora pausada, mas nenhum trabalho será agendado para impressão nessa impressora até que a impressão seja retomada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="31ac1-171">Se uma impressora for desmarcada, todos os trabalhos de impressão dessa impressora serão excluídos, exceto o trabalho de impressão atual.</span><span class="sxs-lookup"><span data-stu-id="31ac1-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="31ac1-172">Se você usar o **Setprinter** para modificar a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) padrão de uma impressora (definindo globalmente os padrões da impressora), deverá primeiro chamar a função [**DocumentProperties**](documentproperties.md) para validar a estrutura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="31ac1-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="31ac1-173">Para as [**estruturas \_ informações \_ da impressora 2**](printer-info-2.md) e [**informações da impressora \_ \_ 3**](printer-info-3.md) que contêm um ponteiro para um descritor de segurança, a função pode definir somente os componentes do descritor de segurança que o chamador tem permissão para modificar.</span><span class="sxs-lookup"><span data-stu-id="31ac1-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="31ac1-174">Para definir componentes específicos do descritor de segurança, você deve especificar os direitos de acesso necessários ao chamar a função [**OpenPrinter**](openprinter.md) ou [**OpenPrinter2**](openprinter2.md) para recuperar um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="31ac1-175">A tabela a seguir mostra os direitos de acesso necessários para modificar os vários componentes do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="31ac1-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="31ac1-176">Permissão de acesso</span><span class="sxs-lookup"><span data-stu-id="31ac1-176">Access permission</span></span>            | <span data-ttu-id="31ac1-177">Componente de descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="31ac1-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="31ac1-178">**proprietário da gravação \_**</span><span class="sxs-lookup"><span data-stu-id="31ac1-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="31ac1-179">Proprietário</span><span class="sxs-lookup"><span data-stu-id="31ac1-179">Owner</span></span><br/> <span data-ttu-id="31ac1-180">Grupo primário</span><span class="sxs-lookup"><span data-stu-id="31ac1-180">Primary group</span></span><br/> |
| <span data-ttu-id="31ac1-181">**GRAVAR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="31ac1-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="31ac1-182">DACL (lista de controle de acesso discricionário)</span><span class="sxs-lookup"><span data-stu-id="31ac1-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="31ac1-183">**\_segurança do sistema de acesso \_**</span><span class="sxs-lookup"><span data-stu-id="31ac1-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="31ac1-184">Lista de controle de acesso (SACL) do sistema</span><span class="sxs-lookup"><span data-stu-id="31ac1-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="31ac1-185">Se o descritor de segurança contiver um componente que o chamador não tem o direito de acesso para modificar, o **Setprinter** falhará.</span><span class="sxs-lookup"><span data-stu-id="31ac1-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="31ac1-186">Os componentes de um descritor de segurança que você não deseja modificar devem ser **nulos** ou não estar presentes, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="31ac1-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="31ac1-187">Se você não quiser modificar o descritor de segurança e chamar **Setprinter** com uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) , defina o membro **pSecurityDescriptor** dessa estrutura como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="31ac1-188">O firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras pode ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="31ac1-189">Se **Setprinter** for chamado por um administrador de máquina, ele habilitará a exceção.</span><span class="sxs-lookup"><span data-stu-id="31ac1-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="31ac1-190">Se ele for chamado por um não administrador e a exceção ainda não tiver sido habilitada, a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="31ac1-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="31ac1-191">Você pode usar o nível 7 com a estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) para publicar, cancelar a publicação ou atualizar os dados do serviço de diretório para a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="31ac1-192">Os dados do serviço de diretório de uma impressora incluem todos os dados armazenados nas \_ \* chaves SPLDS por meio de chamadas para a função [**SetPrinterDataEx**](setprinterdataex.md) para a impressora.</span><span class="sxs-lookup"><span data-stu-id="31ac1-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="31ac1-193">Antes de chamar **Setprinter**, defina o membro **pszObjectGUID** das **informações da impressora \_ \_ 7** como **NULL** e defina o membro *dwAction* como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="31ac1-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="31ac1-194">Valor</span><span class="sxs-lookup"><span data-stu-id="31ac1-194">Value</span></span>                             | <span data-ttu-id="31ac1-195">Descrição</span><span class="sxs-lookup"><span data-stu-id="31ac1-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ac1-196">**publicação do DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="31ac1-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="31ac1-197">Publica os dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="31ac1-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="31ac1-198">**republicação de DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="31ac1-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="31ac1-199">Os dados do serviço de diretório da impressora não são publicados e, em seguida, publicados novamente, atualizando todas as propriedades na impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="31ac1-200">A nova publicação também altera o GUID da impressora publicada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="31ac1-201">Use esse valor se você suspeitar de que os dados publicados da impressora estejam corrompidos.</span><span class="sxs-lookup"><span data-stu-id="31ac1-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="31ac1-202">**DSPRINT \_ Cancelar publicação**</span><span class="sxs-lookup"><span data-stu-id="31ac1-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="31ac1-203">Cancelar a publicação dos dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="31ac1-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="31ac1-204">**atualização do DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="31ac1-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="31ac1-205">Atualiza os dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="31ac1-205">Updates the directory service data.</span></span> <span data-ttu-id="31ac1-206">Isso é o mesmo que o **DSPRINT \_ Publish**, exceto que o **setprinter** falha com o **arquivo de erro \_ \_ não \_ encontrado** se a impressora ainda não estiver publicada.</span><span class="sxs-lookup"><span data-stu-id="31ac1-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="31ac1-207">Use **a \_ atualização do DSPRINT** para atualizar as propriedades publicadas, mas não forçar a publicação.</span><span class="sxs-lookup"><span data-stu-id="31ac1-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="31ac1-208">Os drivers de impressora sempre devem usar a **\_ atualização DSPRINT** em vez de **DSPRINT \_ Publish**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="31ac1-209">**DSPRINT \_ PENDENTE** não é um valor de *dwAction* válido para **setprinter**.</span><span class="sxs-lookup"><span data-stu-id="31ac1-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ac1-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31ac1-210">Requirements</span></span>



| <span data-ttu-id="31ac1-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ac1-211">Requirement</span></span> | <span data-ttu-id="31ac1-212">Valor</span><span class="sxs-lookup"><span data-stu-id="31ac1-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ac1-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31ac1-213">Minimum supported client</span></span><br/> | <span data-ttu-id="31ac1-214">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31ac1-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31ac1-215">Minimum supported server</span></span><br/> | <span data-ttu-id="31ac1-216">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="31ac1-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="31ac1-217">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31ac1-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ac1-218"><dt>WinSpool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="31ac1-219">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31ac1-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="31ac1-220"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="31ac1-221">DLL</span><span class="sxs-lookup"><span data-stu-id="31ac1-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ac1-222"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="31ac1-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="31ac1-223">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="31ac1-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="31ac1-224">**SetPrinterW** (Unicode) e **setprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="31ac1-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="31ac1-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="31ac1-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ac1-226">Impressão</span><span class="sxs-lookup"><span data-stu-id="31ac1-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="31ac1-227">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="31ac1-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="31ac1-228">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="31ac1-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="31ac1-229">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="31ac1-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="31ac1-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="31ac1-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="31ac1-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="31ac1-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="31ac1-232">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="31ac1-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="31ac1-233">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="31ac1-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="31ac1-234">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="31ac1-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="31ac1-235">**Informações da impressora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="31ac1-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="31ac1-236">**Informações da impressora \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="31ac1-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="31ac1-237">**Informações da impressora \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="31ac1-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="31ac1-238">**Informações da impressora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="31ac1-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="31ac1-239">**Informações da impressora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="31ac1-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="31ac1-240">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="31ac1-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




