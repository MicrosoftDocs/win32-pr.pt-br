---
description: Um manipulador de interface do usuário externo pode processar a lista de mensagens do instalador especificado pelo parâmetro dwMessagedFilter da função MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analisando mensagens de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165237"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="8dcae-103">Analisando mensagens de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8dcae-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="8dcae-104">Um manipulador de interface do usuário externo pode processar a lista de mensagens do instalador especificado pelo parâmetro *dwMessagedFilter* da função [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="8dcae-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="8dcae-105">Algumas dessas mensagens contêm cadeias de caracteres que podem ser usadas diretamente, e outras mensagens podem precisar ser analisadas e processadas pelo manipulador de interface do usuário externo para serem úteis.</span><span class="sxs-lookup"><span data-stu-id="8dcae-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="8dcae-106">O manipulador de interface do usuário externa pode precisar apenas monitorar Windows Installer mensagens sem executar nenhuma operação que afete a instalação.</span><span class="sxs-lookup"><span data-stu-id="8dcae-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="8dcae-107">As mensagens de Windows Installer a seguir contêm cadeias de caracteres que podem ser exibidas por uma caixa de diálogo e não precisam de processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="8dcae-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="8dcae-108">Essas mensagens contêm uma lista de botões e ícones que devem ser exibidos por uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8dcae-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="8dcae-109">Você pode usar os valores de **MB \_ ICONMASK**, **MB \_ DEFMASK** e **MB \_ TYPEMASK** para especificar ícones e botões.</span><span class="sxs-lookup"><span data-stu-id="8dcae-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**</span><span class="sxs-lookup"><span data-stu-id="8dcae-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-111">Ocorreu um encerramento prematuro da instalação.</span><span class="sxs-lookup"><span data-stu-id="8dcae-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**erro de INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="8dcae-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-113">Mensagem de erro formatada.</span><span class="sxs-lookup"><span data-stu-id="8dcae-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**aviso de INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="8dcae-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-115">Mensagem de aviso formatada.</span><span class="sxs-lookup"><span data-stu-id="8dcae-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**informações de INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="8dcae-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-117">Mensagem de log formatada.</span><span class="sxs-lookup"><span data-stu-id="8dcae-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_usuário INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="8dcae-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-119">Mensagem de usuário formatada.</span><span class="sxs-lookup"><span data-stu-id="8dcae-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**</span><span class="sxs-lookup"><span data-stu-id="8dcae-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-121">Mensagem formatada indicando uma condição de espaço em disco insuficiente</span><span class="sxs-lookup"><span data-stu-id="8dcae-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="8dcae-122">O manipulador de usuário externo pode usar as seguintes Windows Installer mensagens para monitorar uma sequência da interface do usuário do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8dcae-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="8dcae-123">O instalador envia essas mensagens no início de uma sequência de interface do usuário Windows Installer, uma vez que cada caixa de diálogo é exibida e no final da sequência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8dcae-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="8dcae-124">Nenhum processamento é necessário para usar essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="8dcae-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ encerrar</span><span class="sxs-lookup"><span data-stu-id="8dcae-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-126">Essa mensagem indica o final da sequência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8dcae-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="8dcae-127">A cadeia de caracteres é uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="8dcae-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ inicializar</span><span class="sxs-lookup"><span data-stu-id="8dcae-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-129">Essa mensagem indica que a sequência da interface do usuário foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="8dcae-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="8dcae-130">A cadeia de caracteres é uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="8dcae-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="8dcae-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-132">A cadeia de caracteres contém o nome da caixa de diálogo atual.</span><span class="sxs-lookup"><span data-stu-id="8dcae-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="8dcae-133">As mensagens de Windows Installer a seguir exigem processamento adicional pelo manipulador de interface do usuário externa.</span><span class="sxs-lookup"><span data-stu-id="8dcae-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ resolver**</span><span class="sxs-lookup"><span data-stu-id="8dcae-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-135">O manipulador de interface do usuário externo deve retornar 0 e permitir que Windows Installer manipule a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8dcae-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="8dcae-136">O manipulador de interface do usuário externo pode monitorar essa mensagem, mas não deve executar nenhuma ação que afete a instalação.</span><span class="sxs-lookup"><span data-stu-id="8dcae-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="8dcae-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-138">A interface do usuário externa deve exibir uma [caixa de diálogo FilesInUse](filesinuse-dialog.md) em resposta a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8dcae-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="8dcae-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-140">A interface do usuário externa deve exibir uma [caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) em resposta a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8dcae-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="8dcae-141">Disponível a partir do Windows Installer versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="8dcae-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="8dcae-142">Para obter mais informações sobre essa mensagem, consulte [usando o Gerenciador de reinicialização com uma interface do usuário externa](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="8dcae-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**</span><span class="sxs-lookup"><span data-stu-id="8dcae-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-144">Essa mensagem fornece informações sobre a ação atual.</span><span class="sxs-lookup"><span data-stu-id="8dcae-144">This message gives information about the current action.</span></span> <span data-ttu-id="8dcae-145">O formato é a ação \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="8dcae-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="8dcae-146">\[3 \] , em que um dois-pontos é usado para separar o campo 1 e o campo 2 e um ponto é usado para separar o campo 2 e o campo 3.</span><span class="sxs-lookup"><span data-stu-id="8dcae-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="8dcae-147">O campo \[ 1 \] contém a hora em que a ação foi iniciada usando o formato de propriedade [**time**](time.md) .</span><span class="sxs-lookup"><span data-stu-id="8dcae-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="8dcae-148">O campo \[ 2 \] contém o nome da ação da tabela de sequência.</span><span class="sxs-lookup"><span data-stu-id="8dcae-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="8dcae-149">\[O campo 3 \] fornece a descrição da ação da [tabela ActionText](actiontext-table.md) ou da função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="8dcae-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**</span><span class="sxs-lookup"><span data-stu-id="8dcae-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-151">O formato dessa cadeia de caracteres é especificado pelo valor do [modelo](template.md) fornecido na [tabela ActionText](actiontext-table.md) ou pela função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="8dcae-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="8dcae-152">Pode haver um número ilimitado de mensagens **INSTALLMESSAGE \_ ACTIONDATA** após a mensagem **INSTALLMESSAGE \_ ACTIONSTART** .</span><span class="sxs-lookup"><span data-stu-id="8dcae-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**</span><span class="sxs-lookup"><span data-stu-id="8dcae-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-154">Esta mensagem tem três subtipos: idioma, legenda e CancelShow.</span><span class="sxs-lookup"><span data-stu-id="8dcae-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="8dcae-155">A cadeia de caracteres pode ter três campos delimitados por um número seguido por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="8dcae-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="8dcae-156">Nem todos os campos são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8dcae-156">Not all fields are required.</span></span> <span data-ttu-id="8dcae-157">A mensagem pode ser uma cadeia de caracteres nula ou vazia ("").</span><span class="sxs-lookup"><span data-stu-id="8dcae-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma</span><span class="sxs-lookup"><span data-stu-id="8dcae-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-159">O campo 1 contém o valor 0 para indicar que esta cadeia de caracteres contém informações de idioma.</span><span class="sxs-lookup"><span data-stu-id="8dcae-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="8dcae-160">O campo 2 contém um valor de [idioma](language.md) que é um identificador de idioma numérico (LangID). O campo 3 é um valor que representa uma página de código ANSI.</span><span class="sxs-lookup"><span data-stu-id="8dcae-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Legenda</span><span class="sxs-lookup"><span data-stu-id="8dcae-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-162">O campo 1 contém o valor 1 para indicar que esta cadeia de caracteres contém o texto de uma legenda ou título.</span><span class="sxs-lookup"><span data-stu-id="8dcae-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="8dcae-163">O campo 2 contém texto que um manipulador de interface de usuário externa pode usar como uma legenda de título para uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8dcae-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="8dcae-164">O campo 3 é nulo ou uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="8dcae-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="8dcae-165">O campo 3 pode estar ausente em uma mensagem de legenda.</span><span class="sxs-lookup"><span data-stu-id="8dcae-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span><span class="sxs-lookup"><span data-stu-id="8dcae-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-167">O campo 1 contém o valor 2 para indicar que essa cadeia de caracteres contém informações sobre se o botão Cancelar deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="8dcae-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="8dcae-168">Se o botão Cancelar estiver oculto, o campo 2 conterá o valor 0.</span><span class="sxs-lookup"><span data-stu-id="8dcae-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="8dcae-169">Se o botão Cancelar estiver visível, o campo 2 conterá o valor 1.</span><span class="sxs-lookup"><span data-stu-id="8dcae-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8dcae-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progresso do INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="8dcae-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-171">Esta mensagem tem quatro subtipos: redefinir, ActionInfo, ProgressReport e ProgressAddition.</span><span class="sxs-lookup"><span data-stu-id="8dcae-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="8dcae-172">O manipulador externo não deve agir sobre nenhuma dessas mensagens até que a primeira mensagem de progresso de redefinição seja recebida.</span><span class="sxs-lookup"><span data-stu-id="8dcae-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="8dcae-173">Isso fornece uma estimativa do número total de tiques para a barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Definido</span><span class="sxs-lookup"><span data-stu-id="8dcae-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-175">O campo 1 contém o valor 0 para indicar uma redefinição da barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="8dcae-176">O campo 2 contém o número total de tiques na barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="8dcae-177">O campo 3 contém o valor 0 para o movimento de barra de progresso de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="8dcae-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="8dcae-178">O campo 3 contém o valor 1 para o movimento de barra de progresso regressivo.</span><span class="sxs-lookup"><span data-stu-id="8dcae-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="8dcae-179">O valor 0 no campo 4 significa que a instalação está em andamento e o tempo restante pode ser calculado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="8dcae-180">O valor 1 no campo 4 significa que o script está sendo executado e "Aguarde..." a mensagem pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="8dcae-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="8dcae-181">A estimativa do número total de tiques é uma aproximação e pode ser imprecisa.</span><span class="sxs-lookup"><span data-stu-id="8dcae-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="8dcae-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-183">O campo 1 contém o valor 1 para indicar que esta cadeia de caracteres contém informações de ação.</span><span class="sxs-lookup"><span data-stu-id="8dcae-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="8dcae-184">O campo 2 contém o número de tiques que a barra de progresso move para cada mensagem ActionData enviada pela ação atual.</span><span class="sxs-lookup"><span data-stu-id="8dcae-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="8dcae-185">Se o campo 3 contiver o valor 0, ignore o campo 2.</span><span class="sxs-lookup"><span data-stu-id="8dcae-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="8dcae-186">Se o campo 3 contiver o valor 1, aumente a barra de progresso pelo número de tiques no campo 2 para cada mensagem ActionData enviada pela ação atual.</span><span class="sxs-lookup"><span data-stu-id="8dcae-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="8dcae-187">O campo 4 não é usado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span><span class="sxs-lookup"><span data-stu-id="8dcae-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-189">O campo 1 contém o valor 2 para indicar que essa cadeia de caracteres contém informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="8dcae-190">O campo 2 contém o número de tiques que a barra de progresso moveu.</span><span class="sxs-lookup"><span data-stu-id="8dcae-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="8dcae-191">O campo 3 não é usado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-191">Field 3 is unused.</span></span> <span data-ttu-id="8dcae-192">O campo 4 não é usado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="8dcae-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-194">O campo 1 contém o valor 3 para indicar que uma ação pode adicionar tiques à barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="8dcae-195">O campo 2 contém o número de tiques a serem adicionados à contagem total esperada de tiques de progresso.</span><span class="sxs-lookup"><span data-stu-id="8dcae-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="8dcae-196">O campo 3 não é usado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-196">Field 3 is unused.</span></span> <span data-ttu-id="8dcae-197">O campo 4 não é usado.</span><span class="sxs-lookup"><span data-stu-id="8dcae-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



