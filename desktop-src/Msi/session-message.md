---
description: O método Message do objeto Session executa qualquer operação de registro em log habilitada e adia a execução para o objeto manipulador de interface do usuário associado ao mecanismo. O registro em log pode ser habilitado seletivamente para os vários tipos de mensagem. Consulte o método EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Método Session. Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750217"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="2a0db-105">Método Session. Message</span><span class="sxs-lookup"><span data-stu-id="2a0db-105">Session.Message method</span></span>

<span data-ttu-id="2a0db-106">O método **Message** do objeto [**Session**](session-object.md) executa qualquer operação de registro em log habilitada e adia a execução para o objeto manipulador de interface do usuário associado ao mecanismo.</span><span class="sxs-lookup"><span data-stu-id="2a0db-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="2a0db-107">O registro em log pode ser habilitado seletivamente para os vários tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a0db-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="2a0db-108">Consulte o método [**EnableLog**](installer-enablelog.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0db-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="2a0db-109">Se o campo de registro 0 contiver uma cadeia de caracteres de formatação, ela será usada para formatar os dados nos outros campos.</span><span class="sxs-lookup"><span data-stu-id="2a0db-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="2a0db-110">Caso contrário, se a mensagem for um erro, aviso ou mensagem de usuário, será feita uma tentativa de localizar um modelo de mensagem na tabela de erros do banco de dados atual usando o número de erro encontrado no campo 1 do registro para tipos de mensagem e valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="2a0db-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a0db-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a0db-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="2a0db-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a0db-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a0db-113">*quase*</span><span class="sxs-lookup"><span data-stu-id="2a0db-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0db-114">O parâmetro *Kind* é necessário para ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a0db-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="2a0db-115">Para exibir uma caixa de mensagem com botões e ícones de push, calcule o valor de *tipo* adicionando os estilos de caixa de mensagem padrão usados por [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) e [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiMessageTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="2a0db-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="2a0db-116">Para obter mais informações, consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="2a0db-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="2a0db-117">Constante</span><span class="sxs-lookup"><span data-stu-id="2a0db-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="2a0db-118">Significado</span><span class="sxs-lookup"><span data-stu-id="2a0db-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="2a0db-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="2a0db-120">Encerramento prematuro, possivelmente fatal de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="2a0db-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="2a0db-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="2a0db-122">Mensagem de erro formatada, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a0db-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="2a0db-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="2a0db-124">Mensagem de aviso formatada, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a0db-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="2a0db-125"><dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="2a0db-126">Mensagem de solicitação do usuário, \[ 1 \] é o número da mensagem na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a0db-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="2a0db-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="2a0db-128">Mensagem informativa para log, não a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="2a0db-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="2a0db-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="2a0db-130">Lista de arquivos em uso que precisam ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="2a0db-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="2a0db-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="2a0db-132">Solicitação para determinar um local de origem válido.</span><span class="sxs-lookup"><span data-stu-id="2a0db-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="2a0db-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="2a0db-134">Mensagem de espaço em disco insuficiente.</span><span class="sxs-lookup"><span data-stu-id="2a0db-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="2a0db-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="2a0db-136">Início da ação, \[ 1 \] nome da ação \[ , \] 2 Descrição, \[ 3 \] modelo para mensagens ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="2a0db-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="2a0db-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="2a0db-138">Dados de ação.</span><span class="sxs-lookup"><span data-stu-id="2a0db-138">Action data.</span></span> <span data-ttu-id="2a0db-139">Campos de registro correspondem ao modelo de mensagem ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="2a0db-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="2a0db-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="2a0db-141">Informações da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-141">Progress bar information.</span></span> <span data-ttu-id="2a0db-142">Consulte a descrição dos campos de registro abaixo.</span><span class="sxs-lookup"><span data-stu-id="2a0db-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="2a0db-143"><dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="2a0db-144">Para habilitar o botão Cancelar \[ , defina 1 \] como 2 e \[ 2 \] como 1.</span><span class="sxs-lookup"><span data-stu-id="2a0db-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="2a0db-145">Para desabilitar o botão Cancelar \[ , defina 1 \] como 2 e \[ 2 \] como 0</span><span class="sxs-lookup"><span data-stu-id="2a0db-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a0db-146">*gravável*</span><span class="sxs-lookup"><span data-stu-id="2a0db-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0db-147">Objeto de [**registro**](record-object.md) necessário contendo um campo específico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a0db-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a0db-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a0db-148">Return value</span></span>



| <span data-ttu-id="2a0db-149">Constante</span><span class="sxs-lookup"><span data-stu-id="2a0db-149">Constant</span></span>                                                                                              | <span data-ttu-id="2a0db-150">Valor</span><span class="sxs-lookup"><span data-stu-id="2a0db-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="2a0db-151"><dt>**msiMessageStatusError**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="2a0db-152">-1</span><span class="sxs-lookup"><span data-stu-id="2a0db-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="2a0db-153"><dt>**msiMessageStatusNone**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="2a0db-154">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-155"><dt>**msiMessageStatusOk**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="2a0db-156">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-157"><dt>**msiMessageStatusCancel**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="2a0db-158">2</span><span class="sxs-lookup"><span data-stu-id="2a0db-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-159"><dt>**msiMessageStatusAbort**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="2a0db-160">3</span><span class="sxs-lookup"><span data-stu-id="2a0db-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-161"><dt>**msiMessageStatusRetry**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="2a0db-162">4</span><span class="sxs-lookup"><span data-stu-id="2a0db-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-163"><dt>**msiMessageStatusIgnore**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="2a0db-164">5</span><span class="sxs-lookup"><span data-stu-id="2a0db-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-165"><dt>**msiMessageStatusYes**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="2a0db-166">6</span><span class="sxs-lookup"><span data-stu-id="2a0db-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="2a0db-167"><dt>**msiMessageStatusNo**</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="2a0db-168">7</span><span class="sxs-lookup"><span data-stu-id="2a0db-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2a0db-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a0db-169">Remarks</span></span>

<span data-ttu-id="2a0db-170">**Campos de registro de mensagem**</span><span class="sxs-lookup"><span data-stu-id="2a0db-170">**Message Record Fields**</span></span>

<span data-ttu-id="2a0db-171">O seguinte descreve as definições de campo de registro quando msiMessageTypeProgress é passado como o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a0db-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="2a0db-172">O campo 1 especifica o tipo da mensagem de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="2a0db-173">O significado dos outros campos dependem do valor neste campo.</span><span class="sxs-lookup"><span data-stu-id="2a0db-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="2a0db-174">Os valores possíveis que podem ser definidos no campo 1 são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="2a0db-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="2a0db-175">Nome da mensagem</span><span class="sxs-lookup"><span data-stu-id="2a0db-175">Message name</span></span>     | <span data-ttu-id="2a0db-176">Valor</span><span class="sxs-lookup"><span data-stu-id="2a0db-176">Value</span></span> | <span data-ttu-id="2a0db-177">Descrição do campo 1</span><span class="sxs-lookup"><span data-stu-id="2a0db-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0db-178">MasterReset</span><span class="sxs-lookup"><span data-stu-id="2a0db-178">MasterReset</span></span>      | <span data-ttu-id="2a0db-179">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-179">0</span></span>     | <span data-ttu-id="2a0db-180">Redefine a barra de progresso e define o número total esperado de tiques na barra.</span><span class="sxs-lookup"><span data-stu-id="2a0db-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="2a0db-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="2a0db-181">ActionInfo</span></span>       | <span data-ttu-id="2a0db-182">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-182">1</span></span>     | <span data-ttu-id="2a0db-183">Fornece informações relacionadas às mensagens de progresso a serem enviadas pela ação atual.</span><span class="sxs-lookup"><span data-stu-id="2a0db-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="2a0db-184">ProgressReport</span><span class="sxs-lookup"><span data-stu-id="2a0db-184">ProgressReport</span></span>   | <span data-ttu-id="2a0db-185">2</span><span class="sxs-lookup"><span data-stu-id="2a0db-185">2</span></span>     | <span data-ttu-id="2a0db-186">Incrementa a barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="2a0db-187">ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="2a0db-187">ProgressAddition</span></span> | <span data-ttu-id="2a0db-188">3</span><span class="sxs-lookup"><span data-stu-id="2a0db-188">3</span></span>     | <span data-ttu-id="2a0db-189">Habilita uma ação (como CustomAction) para adicionar tiques ao número total esperado de progresso da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="2a0db-190">O significado do campo 2 depende do valor no campo 1, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a0db-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="2a0db-191">Valor do campo 1</span><span class="sxs-lookup"><span data-stu-id="2a0db-191">Field 1 value</span></span> | <span data-ttu-id="2a0db-192">Descrição do campo 2</span><span class="sxs-lookup"><span data-stu-id="2a0db-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0db-193">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-193">0</span></span>             | <span data-ttu-id="2a0db-194">Número total esperado de tiques na barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="2a0db-195">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-195">1</span></span>             | <span data-ttu-id="2a0db-196">Número de tiques que a barra de progresso move para cada mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="2a0db-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="2a0db-197">Esse campo será ignorado se o campo 3 for 0.</span><span class="sxs-lookup"><span data-stu-id="2a0db-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="2a0db-198">2</span><span class="sxs-lookup"><span data-stu-id="2a0db-198">2</span></span>             | <span data-ttu-id="2a0db-199">Número de tiques movidos pela barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="2a0db-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="2a0db-200">3</span><span class="sxs-lookup"><span data-stu-id="2a0db-200">3</span></span>             | <span data-ttu-id="2a0db-201">Número de tiques a serem adicionados ao progresso total esperado.</span><span class="sxs-lookup"><span data-stu-id="2a0db-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="2a0db-202">O significado do campo 3 depende do valor no campo 1, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a0db-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="2a0db-203">Valor do campo 1</span><span class="sxs-lookup"><span data-stu-id="2a0db-203">Field 1 value</span></span> | <span data-ttu-id="2a0db-204">Valor do campo 3</span><span class="sxs-lookup"><span data-stu-id="2a0db-204">Field 3 value</span></span> | <span data-ttu-id="2a0db-205">Descrição do campo 3</span><span class="sxs-lookup"><span data-stu-id="2a0db-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0db-206">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-206">0</span></span>             | <span data-ttu-id="2a0db-207">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-207">0</span></span>             | <span data-ttu-id="2a0db-208">Barra de progresso de encaminhamento (da esquerda para a direita)</span><span class="sxs-lookup"><span data-stu-id="2a0db-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="2a0db-209">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-209">1</span></span>             | <span data-ttu-id="2a0db-210">Barra de progresso de retrocesso (direita para esquerda)</span><span class="sxs-lookup"><span data-stu-id="2a0db-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="2a0db-211">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-211">1</span></span>             | <span data-ttu-id="2a0db-212">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-212">0</span></span>             | <span data-ttu-id="2a0db-213">A ação atual enviará mensagens ProgressReport explícitas.</span><span class="sxs-lookup"><span data-stu-id="2a0db-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="2a0db-214">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-214">1</span></span>             | <span data-ttu-id="2a0db-215">Incrementar a barra de progresso pelo número de tiques especificado no campo 2 sempre que uma mensagem ActionData for enviada.</span><span class="sxs-lookup"><span data-stu-id="2a0db-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="2a0db-216">2</span><span class="sxs-lookup"><span data-stu-id="2a0db-216">2</span></span>             | <span data-ttu-id="2a0db-217">Não usado</span><span class="sxs-lookup"><span data-stu-id="2a0db-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="2a0db-218">3</span><span class="sxs-lookup"><span data-stu-id="2a0db-218">3</span></span>             | <span data-ttu-id="2a0db-219">Não usado</span><span class="sxs-lookup"><span data-stu-id="2a0db-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="2a0db-220">O significado do campo 4 depende do valor no campo 1, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a0db-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="2a0db-221">Valor do campo 1</span><span class="sxs-lookup"><span data-stu-id="2a0db-221">Field 1 value</span></span> | <span data-ttu-id="2a0db-222">Valor do campo 4</span><span class="sxs-lookup"><span data-stu-id="2a0db-222">Field 4 value</span></span> | <span data-ttu-id="2a0db-223">Descrição do campo 4</span><span class="sxs-lookup"><span data-stu-id="2a0db-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0db-224">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-224">0</span></span>             | <span data-ttu-id="2a0db-225">0</span><span class="sxs-lookup"><span data-stu-id="2a0db-225">0</span></span>             | <span data-ttu-id="2a0db-226">A execução está em andamento.</span><span class="sxs-lookup"><span data-stu-id="2a0db-226">Execution is in progress.</span></span> <span data-ttu-id="2a0db-227">Nesse caso, a interface do usuário pode calcular e exibir o tempo restante.</span><span class="sxs-lookup"><span data-stu-id="2a0db-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="2a0db-228">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-228">1</span></span>             | <span data-ttu-id="2a0db-229">Criando o script de execução.</span><span class="sxs-lookup"><span data-stu-id="2a0db-229">Creating the execution script.</span></span> <span data-ttu-id="2a0db-230">Nesse caso, a interface do usuário pode exibir uma mensagem para aguardar enquanto o instalador termina de preparar a instalação.</span><span class="sxs-lookup"><span data-stu-id="2a0db-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="2a0db-231">1</span><span class="sxs-lookup"><span data-stu-id="2a0db-231">1</span></span>             | <span data-ttu-id="2a0db-232">Não usado</span><span class="sxs-lookup"><span data-stu-id="2a0db-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="2a0db-233">2</span><span class="sxs-lookup"><span data-stu-id="2a0db-233">2</span></span>             | <span data-ttu-id="2a0db-234">Não usado</span><span class="sxs-lookup"><span data-stu-id="2a0db-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="2a0db-235">3</span><span class="sxs-lookup"><span data-stu-id="2a0db-235">3</span></span>             | <span data-ttu-id="2a0db-236">Não usado</span><span class="sxs-lookup"><span data-stu-id="2a0db-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="2a0db-237">**Exibindo caixas de mensagens**</span><span class="sxs-lookup"><span data-stu-id="2a0db-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="2a0db-238">Para exibir uma caixa de mensagem com botões e ícones de push, calcule o valor de *tipo* adicionando os estilos de caixa de mensagem padrão usados por **MessageBox** e **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="2a0db-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="2a0db-239">As opções de botão de ação disponíveis para VBScript são vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ YesNo) e vbRetryCancel (MB \_ RETRYCANCEL).</span><span class="sxs-lookup"><span data-stu-id="2a0db-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="2a0db-240">As opções de ícone disponíveis para VBScript são vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) e vbInformation (MB \_ ICONINFORMATION).</span><span class="sxs-lookup"><span data-stu-id="2a0db-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="2a0db-241">Por exemplo, a chamada a seguir envia uma mensagem **msiMessageTypeError** com os botões ícone VbExclamation e vbYesNo.</span><span class="sxs-lookup"><span data-stu-id="2a0db-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="2a0db-242">Se uma ação personalizada chamar o método **Message** , a ação personalizada deverá ser capaz de manipular um cancelamento pelo usuário e deve retornar **msiDoActionStatusUserExit**.</span><span class="sxs-lookup"><span data-stu-id="2a0db-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a0db-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a0db-243">Requirements</span></span>



| <span data-ttu-id="2a0db-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a0db-244">Requirement</span></span> | <span data-ttu-id="2a0db-245">Valor</span><span class="sxs-lookup"><span data-stu-id="2a0db-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0db-246">Versão</span><span class="sxs-lookup"><span data-stu-id="2a0db-246">Version</span></span><br/> | <span data-ttu-id="2a0db-247">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a0db-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2a0db-248">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a0db-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2a0db-249">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a0db-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2a0db-250">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0db-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a0db-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0db-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2a0db-252">IID</span><span class="sxs-lookup"><span data-stu-id="2a0db-252">IID</span></span><br/>     | <span data-ttu-id="2a0db-253">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2a0db-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
