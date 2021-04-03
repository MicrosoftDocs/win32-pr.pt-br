---
description: As mensagens enviadas usando MsiProcessMessage são as mesmas mensagens que são recebidas pela \_ função de retorno de chamada do manipulador INSTALLUI se MsiSetExternalUI foi chamado.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Enviar mensagens para Windows Installer usando o MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922806"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="6829b-103">Enviando mensagens para Windows Installer usando o MsiProcessMessage</span><span class="sxs-lookup"><span data-stu-id="6829b-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="6829b-104">As mensagens enviadas usando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) são as mesmas mensagens que são recebidas pela função de retorno de chamada do [**\_ manipulador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) se [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="6829b-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="6829b-105">Caso contrário, Windows Installer tratar as mensagens.</span><span class="sxs-lookup"><span data-stu-id="6829b-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="6829b-106">Para obter detalhes, consulte [analisando mensagens de Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="6829b-107">Por exemplo, para enviar uma \_ mensagem de erro INSTALLMESSAGE com o \_ ícone MB ICONWARNING e os \_ botões MB ABORTRETRYCANCEL:</span><span class="sxs-lookup"><span data-stu-id="6829b-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="6829b-108">Em que *hInstall* é o identificador para a instalação, fornecido a uma ação personalizada ou ao identificador *hProduct* de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), e *hRec* é o registro que contém as informações de erro a serem formatadas.</span><span class="sxs-lookup"><span data-stu-id="6829b-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="6829b-109">Para obter informações sobre como a formatação é executada, consulte [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="6829b-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="6829b-110">Por padrão, se uma \_ mensagem de erro INSTALLMESSAGE ou INSTALLMESSAGE \_ FATALEXIT for enviada sem especificar tipos de botão ou de ícone, MB \_ OK, nenhum ícone e MB \_ DEFBUTTON1 serão usados.</span><span class="sxs-lookup"><span data-stu-id="6829b-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="6829b-111">Windows Installer não rotula o botão **abortar** com a cadeia de caracteres "Abort" ao exibir uma MessageBox com a \_ especificação do botão MB ABORTRETRYIGNORE, em vez disso, ela rotula o botão com a cadeia de caracteres "Cancel".</span><span class="sxs-lookup"><span data-stu-id="6829b-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="6829b-112">Todas as mensagens de erro evitem usar a palavra "Abort" e, em vez disso, usar a palavra "Cancel".</span><span class="sxs-lookup"><span data-stu-id="6829b-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="6829b-113">O parâmetro *hRecord* da função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende do tipo de mensagem enviado para o [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="6829b-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="6829b-114">A lista a seguir detalha os requisitos do registro em relação ao tipo de mensagem:</span><span class="sxs-lookup"><span data-stu-id="6829b-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="6829b-115">INSTALLMESSAGE \_ FATALEXIT</span><span class="sxs-lookup"><span data-stu-id="6829b-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="6829b-116">informações de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="6829b-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="6829b-117">INSTALLMESSAGE \_ OUTOFDISKSPACE</span><span class="sxs-lookup"><span data-stu-id="6829b-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="6829b-118">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-118">Field</span></span>         | <span data-ttu-id="6829b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-120">0</span><span class="sxs-lookup"><span data-stu-id="6829b-120">0</span></span>             | <span data-ttu-id="6829b-121">Modelo para a formatação da cadeia de caracteres resultante.</span><span class="sxs-lookup"><span data-stu-id="6829b-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="6829b-122">Consulte [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6829b-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="6829b-123">Os campos do registro são referenciados usando \[ 1 \] para o campo 1, \[ 2 \] para o campo 2, etc.</span><span class="sxs-lookup"><span data-stu-id="6829b-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="6829b-124">1 a *n*</span><span class="sxs-lookup"><span data-stu-id="6829b-124">1 through *n*</span></span> | <span data-ttu-id="6829b-125">Todos os campos subsequentes estão diretamente relacionados aos campos referenciados pelo modelo no campo 0.</span><span class="sxs-lookup"><span data-stu-id="6829b-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="6829b-126">Se o campo 0 for nulo, a cadeia de caracteres recebida pelo manipulador de interface do usuário será formatada como: 1: \[ dados do campo 1 \] 2: \[ dados do campo 2, \] o que significa que, para cada campo do registro, a cadeia de caracteres contém o número do campo seguido pelos dados armazenados no campo.</span><span class="sxs-lookup"><span data-stu-id="6829b-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="6829b-127">As mensagens de informações de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) são registradas quando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), a [opção de linha de comando](command-line-options.md)'/l ' ou a [política de registro](logging.md) especifica ' I ' ou informações de INSTALLLOGMODE \_ .</span><span class="sxs-lookup"><span data-stu-id="6829b-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="6829b-128">erro de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="6829b-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="6829b-129">aviso de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="6829b-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="6829b-130">\_usuário INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="6829b-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="6829b-131">Para usar uma mensagem da tabela de erros.</span><span class="sxs-lookup"><span data-stu-id="6829b-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="6829b-132">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-132">Field</span></span>         | <span data-ttu-id="6829b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="6829b-134">0</span><span class="sxs-lookup"><span data-stu-id="6829b-134">0</span></span>             | <span data-ttu-id="6829b-135">Deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="6829b-135">Must be null.</span></span>                                         |
| <span data-ttu-id="6829b-136">1</span><span class="sxs-lookup"><span data-stu-id="6829b-136">1</span></span>             | <span data-ttu-id="6829b-137">Número da mensagem na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="6829b-138">2 a *n*</span><span class="sxs-lookup"><span data-stu-id="6829b-138">2 through *n*</span></span> | <span data-ttu-id="6829b-139">Relacionado à mensagem especificada na tabela de erros.</span><span class="sxs-lookup"><span data-stu-id="6829b-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="6829b-140">Por exemplo.</span><span class="sxs-lookup"><span data-stu-id="6829b-140">For example.</span></span>



| <span data-ttu-id="6829b-141">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-141">Field</span></span> | <span data-ttu-id="6829b-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="6829b-142">Type</span></span>   | <span data-ttu-id="6829b-143">Dados</span><span class="sxs-lookup"><span data-stu-id="6829b-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="6829b-144">0</span><span class="sxs-lookup"><span data-stu-id="6829b-144">0</span></span>     | <span data-ttu-id="6829b-145">string</span><span class="sxs-lookup"><span data-stu-id="6829b-145">string</span></span> | <span data-ttu-id="6829b-146">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-146">null</span></span>       |
| <span data-ttu-id="6829b-147">1</span><span class="sxs-lookup"><span data-stu-id="6829b-147">1</span></span>     | <span data-ttu-id="6829b-148">INT</span><span class="sxs-lookup"><span data-stu-id="6829b-148">int</span></span>    | <span data-ttu-id="6829b-149">1304</span><span class="sxs-lookup"><span data-stu-id="6829b-149">1304</span></span>       |
| <span data-ttu-id="6829b-150">2</span><span class="sxs-lookup"><span data-stu-id="6829b-150">2</span></span>     | <span data-ttu-id="6829b-151">string</span><span class="sxs-lookup"><span data-stu-id="6829b-151">string</span></span> | <span data-ttu-id="6829b-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="6829b-152">Myfile.txt</span></span> |



 

<span data-ttu-id="6829b-153">A mensagem resultante recebida do manipulador de interface do usuário é:</span><span class="sxs-lookup"><span data-stu-id="6829b-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="6829b-154">Erro 1304.</span><span class="sxs-lookup"><span data-stu-id="6829b-154">Error 1304.</span></span> <span data-ttu-id="6829b-155">Erro ao gravar no arquivo: Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="6829b-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="6829b-156">Verifique se você tem acesso a esse diretório.</span><span class="sxs-lookup"><span data-stu-id="6829b-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="6829b-157">Se o campo 0 não for nulo, a mensagem da tabela de erros será substituída.</span><span class="sxs-lookup"><span data-stu-id="6829b-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="6829b-158">Em vez disso, o modelo campo 0 determina o formato da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6829b-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="6829b-159">A mensagem também pode especificar os botões, incluindo o botão padrão e o ícone a ser usado com a mensagem, conforme mencionado acima.</span><span class="sxs-lookup"><span data-stu-id="6829b-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="6829b-160">Os tipos de botão e ícone são listados [**no \_ manipulador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span><span class="sxs-lookup"><span data-stu-id="6829b-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="6829b-161">INSTALLMESSAGE \_ COMMONDATA</span><span class="sxs-lookup"><span data-stu-id="6829b-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="6829b-162">Essa mensagem é enviada para habilitar ou desabilitar o botão **Cancelar** em uma caixa de diálogo de progresso.</span><span class="sxs-lookup"><span data-stu-id="6829b-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="6829b-163">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-163">Field</span></span> | <span data-ttu-id="6829b-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-165">0</span><span class="sxs-lookup"><span data-stu-id="6829b-165">0</span></span>     | <span data-ttu-id="6829b-166">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="6829b-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="6829b-167">1</span><span class="sxs-lookup"><span data-stu-id="6829b-167">1</span></span>     | <span data-ttu-id="6829b-168">2 refere-se ao botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="6829b-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="6829b-169">2</span><span class="sxs-lookup"><span data-stu-id="6829b-169">2</span></span>     | <span data-ttu-id="6829b-170">Um valor de 1 indica que o botão de **cancelamento** deve estar visível.</span><span class="sxs-lookup"><span data-stu-id="6829b-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="6829b-171">Um valor de 0 indica que o botão de **cancelamento** deve ser invisível.</span><span class="sxs-lookup"><span data-stu-id="6829b-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="6829b-172">Por exemplo, para desabilitar ou ocultar o botão **Cancelar** , o registro seria exibido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6829b-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="6829b-173">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-173">Field</span></span> | <span data-ttu-id="6829b-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="6829b-174">Type</span></span>   | <span data-ttu-id="6829b-175">Dados</span><span class="sxs-lookup"><span data-stu-id="6829b-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="6829b-176">0</span><span class="sxs-lookup"><span data-stu-id="6829b-176">0</span></span>     | <span data-ttu-id="6829b-177">string</span><span class="sxs-lookup"><span data-stu-id="6829b-177">string</span></span> | <span data-ttu-id="6829b-178">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-178">null</span></span> |
| <span data-ttu-id="6829b-179">1</span><span class="sxs-lookup"><span data-stu-id="6829b-179">1</span></span>     | <span data-ttu-id="6829b-180">INT</span><span class="sxs-lookup"><span data-stu-id="6829b-180">int</span></span>    | <span data-ttu-id="6829b-181">2</span><span class="sxs-lookup"><span data-stu-id="6829b-181">2</span></span>    |
| <span data-ttu-id="6829b-182">2</span><span class="sxs-lookup"><span data-stu-id="6829b-182">2</span></span>     | <span data-ttu-id="6829b-183">INT</span><span class="sxs-lookup"><span data-stu-id="6829b-183">int</span></span>    | <span data-ttu-id="6829b-184">0</span><span class="sxs-lookup"><span data-stu-id="6829b-184">0</span></span>    |



 

<span data-ttu-id="6829b-185">INSTALLMESSAGE \_ ACTIONSTART</span><span class="sxs-lookup"><span data-stu-id="6829b-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="6829b-186">INSTALLMESSAGE \_ ACTIONDATA</span><span class="sxs-lookup"><span data-stu-id="6829b-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="6829b-187">O \_ registro INSTALLMESSAGE ACTIONSTART determina o formato do registro ActionData.</span><span class="sxs-lookup"><span data-stu-id="6829b-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="6829b-188">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-188">Field</span></span> | <span data-ttu-id="6829b-189">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-190">0</span><span class="sxs-lookup"><span data-stu-id="6829b-190">0</span></span>     | <span data-ttu-id="6829b-191">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-191">null</span></span>                                                                                                          |
| <span data-ttu-id="6829b-192">1</span><span class="sxs-lookup"><span data-stu-id="6829b-192">1</span></span>     | <span data-ttu-id="6829b-193">Nome da ação.</span><span class="sxs-lookup"><span data-stu-id="6829b-193">Action name.</span></span> <span data-ttu-id="6829b-194">O nome neste campo deve ser não nulo.</span><span class="sxs-lookup"><span data-stu-id="6829b-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="6829b-195">2</span><span class="sxs-lookup"><span data-stu-id="6829b-195">2</span></span>     | <span data-ttu-id="6829b-196">Descrição da ação.</span><span class="sxs-lookup"><span data-stu-id="6829b-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="6829b-197">3</span><span class="sxs-lookup"><span data-stu-id="6829b-197">3</span></span>     | <span data-ttu-id="6829b-198">Modelo de ação.</span><span class="sxs-lookup"><span data-stu-id="6829b-198">Action template.</span></span> <span data-ttu-id="6829b-199">Isso é usado para o ActionData cuja mensagem está sendo formatada de acordo com este modelo.</span><span class="sxs-lookup"><span data-stu-id="6829b-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="6829b-200">Não referencie o campo 0 na mensagem do modelo de ação.</span><span class="sxs-lookup"><span data-stu-id="6829b-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="6829b-201">O \_ registro INSTALLMESSAGE ACTIONDATA é formatado da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6829b-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="6829b-202">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-202">Field</span></span>         | <span data-ttu-id="6829b-203">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-204">0</span><span class="sxs-lookup"><span data-stu-id="6829b-204">0</span></span>             | <span data-ttu-id="6829b-205">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="6829b-206">1 a *n*</span><span class="sxs-lookup"><span data-stu-id="6829b-206">1 through *n*</span></span> | <span data-ttu-id="6829b-207">Dependendo do campo 3 da \_ mensagem ou do modelo ACTIONSTART INSTALLMESSAGE correspondente especificado na [tabela ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="6829b-208">Por exemplo, o \_ registro INSTALLMESSAGE ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="6829b-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="6829b-209">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-209">Field</span></span> | <span data-ttu-id="6829b-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="6829b-210">Type</span></span>   | <span data-ttu-id="6829b-211">Dados</span><span class="sxs-lookup"><span data-stu-id="6829b-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="6829b-212">0</span><span class="sxs-lookup"><span data-stu-id="6829b-212">0</span></span>     | <span data-ttu-id="6829b-213">string</span><span class="sxs-lookup"><span data-stu-id="6829b-213">string</span></span> | <span data-ttu-id="6829b-214">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-214">null</span></span>                                                            |
| <span data-ttu-id="6829b-215">1</span><span class="sxs-lookup"><span data-stu-id="6829b-215">1</span></span>     | <span data-ttu-id="6829b-216">string</span><span class="sxs-lookup"><span data-stu-id="6829b-216">string</span></span> | <span data-ttu-id="6829b-217">Myaction</span><span class="sxs-lookup"><span data-stu-id="6829b-217">MyAction</span></span>                                                        |
| <span data-ttu-id="6829b-218">2</span><span class="sxs-lookup"><span data-stu-id="6829b-218">2</span></span>     | <span data-ttu-id="6829b-219">string</span><span class="sxs-lookup"><span data-stu-id="6829b-219">string</span></span> | <span data-ttu-id="6829b-220">Esta é a descrição de "myaction"</span><span class="sxs-lookup"><span data-stu-id="6829b-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="6829b-221">3</span><span class="sxs-lookup"><span data-stu-id="6829b-221">3</span></span>     | <span data-ttu-id="6829b-222">string</span><span class="sxs-lookup"><span data-stu-id="6829b-222">string</span></span> | <span data-ttu-id="6829b-223">Modelo myaction: os dados de field1 são \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="6829b-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="6829b-224">os dados do campo 2 são \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="6829b-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="6829b-225">O modelo para INSTALLMESSAGE \_ ACTIONSTART (campo 3) faz referência aos campos 1 e 2, o registro de ACTIONDATA de INSTALLMESSAGE \_ deve ter dois campos contendo os dados garantidos.</span><span class="sxs-lookup"><span data-stu-id="6829b-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="6829b-226">Os campos podem ser campos de cadeia de caracteres ou inteiros.</span><span class="sxs-lookup"><span data-stu-id="6829b-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="6829b-227">\_Registro de ACTIONDATA INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="6829b-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="6829b-228">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-228">Field</span></span> | <span data-ttu-id="6829b-229">Tipo</span><span class="sxs-lookup"><span data-stu-id="6829b-229">Type</span></span>   | <span data-ttu-id="6829b-230">Dados</span><span class="sxs-lookup"><span data-stu-id="6829b-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="6829b-231">0</span><span class="sxs-lookup"><span data-stu-id="6829b-231">0</span></span>     | <span data-ttu-id="6829b-232">string</span><span class="sxs-lookup"><span data-stu-id="6829b-232">string</span></span> | <span data-ttu-id="6829b-233">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-233">null</span></span>                    |
| <span data-ttu-id="6829b-234">1</span><span class="sxs-lookup"><span data-stu-id="6829b-234">1</span></span>     | <span data-ttu-id="6829b-235">INT</span><span class="sxs-lookup"><span data-stu-id="6829b-235">int</span></span>    | <span data-ttu-id="6829b-236">2</span><span class="sxs-lookup"><span data-stu-id="6829b-236">2</span></span>                       |
| <span data-ttu-id="6829b-237">2</span><span class="sxs-lookup"><span data-stu-id="6829b-237">2</span></span>     | <span data-ttu-id="6829b-238">string</span><span class="sxs-lookup"><span data-stu-id="6829b-238">string</span></span> | <span data-ttu-id="6829b-239">ActionData para myaction</span><span class="sxs-lookup"><span data-stu-id="6829b-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="6829b-240">INSTALLMESSAGE \_ FILESINUSE</span><span class="sxs-lookup"><span data-stu-id="6829b-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="6829b-241">O registro FILESINUSE é um registro de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="6829b-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="6829b-242">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-242">Field</span></span> | <span data-ttu-id="6829b-243">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-244">0</span><span class="sxs-lookup"><span data-stu-id="6829b-244">0</span></span>     | <span data-ttu-id="6829b-245">Este campo pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="6829b-245">This field can be null.</span></span> <span data-ttu-id="6829b-246">Para uma instalação usando uma interface do usuário básica, esse campo pode especificar texto estático para exibição no [controle ListBox](listbox-control.md) da [caixa de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="6829b-247">Para uma instalação usando uma interface do usuário completa, esse campo não tem efeito porque o texto é especificado pela criação da caixa de diálogo FilesInUse personalizada.</span><span class="sxs-lookup"><span data-stu-id="6829b-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="6829b-248">1</span><span class="sxs-lookup"><span data-stu-id="6829b-248">1</span></span>     | <span data-ttu-id="6829b-249">Nome do arquivo em uso.</span><span class="sxs-lookup"><span data-stu-id="6829b-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6829b-250">2</span><span class="sxs-lookup"><span data-stu-id="6829b-250">2</span></span>     | <span data-ttu-id="6829b-251">Este campo identifica o processo que contém o arquivo em uso. **Windows Installer versão 4,0:** A ID do processo (PID) do processo ou o título da janela do processo.</span><span class="sxs-lookup"><span data-stu-id="6829b-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="6829b-252">**Windows Installer versão 3,1 e anteriores:** Esse campo deve ser a identificação do processo (PID) do processo.</span><span class="sxs-lookup"><span data-stu-id="6829b-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="6829b-253">Por exemplo, para enviar uma mensagem FilesInUse mostrando dois arquivos em uso, red.exe e blue.exe, o registro tem quatro campos mais o campo 0.</span><span class="sxs-lookup"><span data-stu-id="6829b-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="6829b-254">O formato do registro seria como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6829b-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="6829b-255">Este exemplo requer Windows Installer versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="6829b-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="6829b-256">**Windows Installer versão 3,1 e anteriores:** Os campos 2 e 4 no exemplo a seguir devem conter os PIDs dos processos que mantêm red.exe e blue.exe em uso.</span><span class="sxs-lookup"><span data-stu-id="6829b-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="6829b-257">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-257">Field</span></span> | <span data-ttu-id="6829b-258">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="6829b-259">0</span><span class="sxs-lookup"><span data-stu-id="6829b-259">0</span></span>     | <span data-ttu-id="6829b-260">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-260">null</span></span>              |
| <span data-ttu-id="6829b-261">1</span><span class="sxs-lookup"><span data-stu-id="6829b-261">1</span></span>     | <span data-ttu-id="6829b-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="6829b-262">Red.exe</span></span>           |
| <span data-ttu-id="6829b-263">2</span><span class="sxs-lookup"><span data-stu-id="6829b-263">2</span></span>     | <span data-ttu-id="6829b-264">Título da janela vermelha</span><span class="sxs-lookup"><span data-stu-id="6829b-264">Red Window Title</span></span>  |
| <span data-ttu-id="6829b-265">3</span><span class="sxs-lookup"><span data-stu-id="6829b-265">3</span></span>     | <span data-ttu-id="6829b-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="6829b-266">Blue.exe</span></span>          |
| <span data-ttu-id="6829b-267">4</span><span class="sxs-lookup"><span data-stu-id="6829b-267">4</span></span>     | <span data-ttu-id="6829b-268">Título da janela azul</span><span class="sxs-lookup"><span data-stu-id="6829b-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="6829b-269">No Windows Installer versão 4,0, se a PID passada do serviço não tiver um título de janela, como um aplicativo de bandeja do sistema, o arquivo não será exibido e o log detalhado conterá as mensagens a seguir.</span><span class="sxs-lookup"><span data-stu-id="6829b-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="6829b-270">INSTALLMESSAGE \_ resolver</span><span class="sxs-lookup"><span data-stu-id="6829b-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="6829b-271">O \_ registro de resolução INSTALLMESSAGE tem sete campos.</span><span class="sxs-lookup"><span data-stu-id="6829b-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="6829b-272">Para \_ que o resolvedor de INSTALLMESSAGE funcione corretamente, um manipulador de interface do usuário externa pode não manipular a \_ mensagem de resolução INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="6829b-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="6829b-273">Windows Installer deve manipular a \_ mensagem de resolução INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="6829b-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="6829b-274">Ou seja, o manipulador de interface do usuário externa retorna 0 para indicar "nenhuma ação tomada" ao filtrar a \_ mensagem de resolução INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="6829b-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="6829b-275">A prática recomendada é evitar o envio de uma mensagem de resolução.</span><span class="sxs-lookup"><span data-stu-id="6829b-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="6829b-276">Campo</span><span class="sxs-lookup"><span data-stu-id="6829b-276">Field</span></span> | <span data-ttu-id="6829b-277">Descrição</span><span class="sxs-lookup"><span data-stu-id="6829b-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6829b-278">0</span><span class="sxs-lookup"><span data-stu-id="6829b-278">0</span></span>     | <span data-ttu-id="6829b-279">nulo</span><span class="sxs-lookup"><span data-stu-id="6829b-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="6829b-280">1</span><span class="sxs-lookup"><span data-stu-id="6829b-280">1</span></span>     | <span data-ttu-id="6829b-281">null</span><span class="sxs-lookup"><span data-stu-id="6829b-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="6829b-282">2</span><span class="sxs-lookup"><span data-stu-id="6829b-282">2</span></span>     | <span data-ttu-id="6829b-283">Nome do pacote.</span><span class="sxs-lookup"><span data-stu-id="6829b-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="6829b-284">3</span><span class="sxs-lookup"><span data-stu-id="6829b-284">3</span></span>     | <span data-ttu-id="6829b-285">Código do produto.</span><span class="sxs-lookup"><span data-stu-id="6829b-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="6829b-286">4</span><span class="sxs-lookup"><span data-stu-id="6829b-286">4</span></span>     | <span data-ttu-id="6829b-287">O caminho relativo, se conhecido, pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="6829b-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="6829b-288">5</span><span class="sxs-lookup"><span data-stu-id="6829b-288">5</span></span>     | <span data-ttu-id="6829b-289">0</span><span class="sxs-lookup"><span data-stu-id="6829b-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6829b-290">6</span><span class="sxs-lookup"><span data-stu-id="6829b-290">6</span></span>     | <span data-ttu-id="6829b-291">Se o código do pacote deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="6829b-291">Whether to validate the package code.</span></span> <span data-ttu-id="6829b-292">Um valor de ' 1 ' indica que o código do pacote deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="6829b-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="6829b-293">Um valor de ' 0 ' indica que o pacote não deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="6829b-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="6829b-294">7</span><span class="sxs-lookup"><span data-stu-id="6829b-294">7</span></span>     | <span data-ttu-id="6829b-295">Disco necessário da tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="6829b-295">Required disk from media table.</span></span> <span data-ttu-id="6829b-296">Um valor de ' 0 ' indica que qualquer disco é aceitável.</span><span class="sxs-lookup"><span data-stu-id="6829b-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




