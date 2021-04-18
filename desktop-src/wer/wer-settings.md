---
title: Configurações WER
description: Configurações para personalizar a experiência de relatório de problemas. Todas essas configurações podem ser definidas usando Política de Grupo. Alguns também podem ser alterados na central de ações para Windows 7 e Windows 8. Para o Windows 10, use a função de pesquisa em configurações para localizar exibir configurações avançadas do sistema.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Relatório de Erros do Windows de relatório de erros do Windows, configurações
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "105751388"
---
# <a name="wer-settings"></a><span data-ttu-id="bb2af-107">Configurações WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-107">WER Settings</span></span>

<span data-ttu-id="bb2af-108">Relatório de Erros do Windows (WER) fornece muitas configurações para personalizar a experiência de relatório de problemas.</span><span class="sxs-lookup"><span data-stu-id="bb2af-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="bb2af-109">Todas essas configurações podem ser definidas usando Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="bb2af-110">Alguns também podem ser alterados na **central de ações** para Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb2af-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="bb2af-111">Para o Windows 10, use a função de pesquisa em configurações para localizar **exibir configurações avançadas do sistema**.</span><span class="sxs-lookup"><span data-stu-id="bb2af-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="bb2af-112">As configurações do WER estão localizadas em uma das seguintes subchaves do registro:</span><span class="sxs-lookup"><span data-stu-id="bb2af-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="bb2af-113">**HKEY \_ Software de \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **relatório de erros do Windows**</span><span class="sxs-lookup"><span data-stu-id="bb2af-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="bb2af-114">**HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **relatório de erros do Windows**</span><span class="sxs-lookup"><span data-stu-id="bb2af-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="bb2af-115">Subchave Relatório de Erros do Windows</span><span class="sxs-lookup"><span data-stu-id="bb2af-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="bb2af-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span><span class="sxs-lookup"><span data-stu-id="bb2af-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-117">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-118">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="bb2af-119">0-desabilitar limitação de bypass de dados.</span><span class="sxs-lookup"><span data-stu-id="bb2af-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="bb2af-120">Se o bypass estiver desabilitado ou não estiver configurado como uma configuração de política, o WER restringirá os dados por padrão.</span><span class="sxs-lookup"><span data-stu-id="bb2af-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="bb2af-121">O WER não carrega mais de um arquivo CAB para um relatório que contém dados sobre os mesmos tipos de evento.</span><span class="sxs-lookup"><span data-stu-id="bb2af-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="bb2af-122">1-Habilitar limitação de bypass de dados.</span><span class="sxs-lookup"><span data-stu-id="bb2af-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="bb2af-123">O WER não acelera os dados.</span><span class="sxs-lookup"><span data-stu-id="bb2af-123">WER does not throttle data.</span></span> <span data-ttu-id="bb2af-124">O WER carrega arquivos CAB adicionais que podem conter dados sobre os mesmos tipos de evento que um relatório carregado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bb2af-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="bb2af-125">Se deseja habilitar o bypass da limitação de dados do cliente do WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span><span class="sxs-lookup"><span data-stu-id="bb2af-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-127">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-127">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-128">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-128">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-129">1-somente parâmetros (padrão no Windows 7)</span><span class="sxs-lookup"><span data-stu-id="bb2af-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="bb2af-130">2-todos os dados (padrão no Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="bb2af-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="bb2af-131">Se os parâmetros devem ser arquivados somente ou todos os dados</span><span class="sxs-lookup"><span data-stu-id="bb2af-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Autorização \\ de consentimento**</span><span class="sxs-lookup"><span data-stu-id="bb2af-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-133">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-133">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-134">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-134">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-135">1-sempre perguntar (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="bb2af-136">2-somente parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb2af-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="bb2af-137">3-parâmetros e dados seguros</span><span class="sxs-lookup"><span data-stu-id="bb2af-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="bb2af-138">4-todos os dados</span><span class="sxs-lookup"><span data-stu-id="bb2af-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="bb2af-139">Opção de consentimento padrão</span><span class="sxs-lookup"><span data-stu-id="bb2af-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentimento \\**</span><span class="sxs-lookup"><span data-stu-id="bb2af-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-141">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-141">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-142">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-142">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-143">0-o consentimento vertical substituirá o consentimento padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="bb2af-144">1-o consentimento padrão substituirá o consentimento específico do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bb2af-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="bb2af-145">Se o consentimento padrão substitui o consentimento vertical</span><span class="sxs-lookup"><span data-stu-id="bb2af-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Vertical do consentimento \\ \[\]**</span><span class="sxs-lookup"><span data-stu-id="bb2af-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-147">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-148">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-148">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-149">1-sempre perguntar (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="bb2af-150">2-somente parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb2af-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="bb2af-151">3-parâmetros e dados seguros</span><span class="sxs-lookup"><span data-stu-id="bb2af-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="bb2af-152">4-todos os dados</span><span class="sxs-lookup"><span data-stu-id="bb2af-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="bb2af-153">Opção de consentimento para o plug-in do WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span><span class="sxs-lookup"><span data-stu-id="bb2af-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-155">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="bb2af-155">**REG\_SZ**</span></span>

<span data-ttu-id="bb2af-156">O caminho do diretório</span><span class="sxs-lookup"><span data-stu-id="bb2af-156">The directory path</span></span>

<span data-ttu-id="bb2af-157">Diretório de destino no servidor</span><span class="sxs-lookup"><span data-stu-id="bb2af-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span><span class="sxs-lookup"><span data-stu-id="bb2af-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-159">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-159">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-160">O número da porta</span><span class="sxs-lookup"><span data-stu-id="bb2af-160">The port number</span></span>

<span data-ttu-id="bb2af-161">Número da porta a ser usada com o servidor corporativo</span><span class="sxs-lookup"><span data-stu-id="bb2af-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span><span class="sxs-lookup"><span data-stu-id="bb2af-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-163">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="bb2af-163">**REG\_SZ**</span></span>

<span data-ttu-id="bb2af-164">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="bb2af-164">The name of the server</span></span>

<span data-ttu-id="bb2af-165">Nome do servidor corporativo</span><span class="sxs-lookup"><span data-stu-id="bb2af-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span><span class="sxs-lookup"><span data-stu-id="bb2af-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-167">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-167">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-168">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-168">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-169">0-não (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="bb2af-170">1 – Sim</span><span class="sxs-lookup"><span data-stu-id="bb2af-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="bb2af-171">Se a autenticação integrada do Windows deve ser usada</span><span class="sxs-lookup"><span data-stu-id="bb2af-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span><span class="sxs-lookup"><span data-stu-id="bb2af-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-173">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-173">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-174">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-174">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-175">0-não (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="bb2af-176">1 – Sim</span><span class="sxs-lookup"><span data-stu-id="bb2af-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="bb2af-177">Se o SSL deve ser usado</span><span class="sxs-lookup"><span data-stu-id="bb2af-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ EXEName \] (substitua " \[ EXEName \] " por um nome real de um arquivo. exe, por exemplo, "notepad.exe")**</span><span class="sxs-lookup"><span data-stu-id="bb2af-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-179">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-180">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="bb2af-181">0-processos com um nome de imagem executável de **\[ EXEName \]** não exigem que o usuário escolha **depurar** ou **continuar** (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="bb2af-182">1-processos com um nome de imagem executável de **\[ EXEName \]** exigem que o usuário escolha **depurar** ou **continuar**</span><span class="sxs-lookup"><span data-stu-id="bb2af-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="bb2af-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " é o nome do valor literal)**</span><span class="sxs-lookup"><span data-stu-id="bb2af-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-184">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-184">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-185">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="bb2af-186">0-todos os processos, exceto aqueles especificados explicitamente na configuração **DebugApplications \\ \[ \] EXEName** não exigem que o usuário escolha **depurar** ou **continuar** (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="bb2af-187">1-todos os processos, exceto aqueles especificados explicitamente na configuração **DebugApplications \\ \[ \] EXEName** exigem que o usuário escolha **depurar** ou **continuar**</span><span class="sxs-lookup"><span data-stu-id="bb2af-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="bb2af-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span><span class="sxs-lookup"><span data-stu-id="bb2af-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-189">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-189">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-190">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-190">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-191">0 - Habilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="bb2af-192">1 - Desabilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="bb2af-193">Habilitar ou desabilitar o arquivo morto</span><span class="sxs-lookup"><span data-stu-id="bb2af-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="bb2af-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-195">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-195">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-196">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-196">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-197">0-habilitado (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="bb2af-198">1 - Desabilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="bb2af-199">Habilitar ou desabilitar o WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span><span class="sxs-lookup"><span data-stu-id="bb2af-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-201">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-201">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-202">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-202">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-203">0 - Habilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="bb2af-204">1 - Desabilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="bb2af-205">Habilitar ou desabilitar o enfileiramento de relatórios</span><span class="sxs-lookup"><span data-stu-id="bb2af-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="bb2af-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-207">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-207">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-208">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-208">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-209">0-interface do usuário (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="bb2af-210">1-sem interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bb2af-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="bb2af-211">Habilitar ou desabilitar a interface do usuário do WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span><span class="sxs-lookup"><span data-stu-id="bb2af-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-213">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-213">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-214">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-214">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-215">0-enviar (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="bb2af-216">1-não enviar</span><span class="sxs-lookup"><span data-stu-id="bb2af-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="bb2af-217">Se deseja impedir o envio de dados de segundo nível</span><span class="sxs-lookup"><span data-stu-id="bb2af-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Nome do aplicativo ExcludedApplications\]**</span><span class="sxs-lookup"><span data-stu-id="bb2af-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-219">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="bb2af-219">**REG\_SZ**</span></span>

<span data-ttu-id="bb2af-220">Usar [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="bb2af-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="bb2af-221">Lista de aplicativos excluídos</span><span class="sxs-lookup"><span data-stu-id="bb2af-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span><span class="sxs-lookup"><span data-stu-id="bb2af-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-223">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-223">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-224">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-224">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-225">0-não (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="bb2af-226">1 – Sim</span><span class="sxs-lookup"><span data-stu-id="bb2af-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="bb2af-227">Se deseja enviar todos os relatórios para a fila do usuário</span><span class="sxs-lookup"><span data-stu-id="bb2af-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\** Nome do **aplicativo DumpFolder ou LocalDumps \\ \[ \] \\ DumpFolder**</span><span class="sxs-lookup"><span data-stu-id="bb2af-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-229">**REG \_ expande \_ sz**</span><span class="sxs-lookup"><span data-stu-id="bb2af-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="bb2af-230">O caminho do diretório.</span><span class="sxs-lookup"><span data-stu-id="bb2af-230">The directory path.</span></span> <span data-ttu-id="bb2af-231">O valor padrão é% LOCALAPPDATA% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="bb2af-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="bb2af-232">Se o padrão não for usado, o aplicativo deverá garantir que a pasta tenha uma ACL suficiente.</span><span class="sxs-lookup"><span data-stu-id="bb2af-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="bb2af-233">**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="bb2af-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="bb2af-234">Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bb2af-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="bb2af-235">O caminho onde os arquivos de despejo devem ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="bb2af-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="bb2af-236">Observe que as configurações por processo substituirão as configurações globais existentes para obter mais informações, consulte [coletando despejos de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="bb2af-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="bb2af-237">Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.</span><span class="sxs-lookup"><span data-stu-id="bb2af-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\** Nome do **aplicativo DumpCount ou LocalDumps \\ \[ \] \\ DumpCount**</span><span class="sxs-lookup"><span data-stu-id="bb2af-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-239">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-239">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-240">O número máximo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-240">The maximum number.</span></span> <span data-ttu-id="bb2af-241">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="bb2af-241">The default is 10.</span></span> <span data-ttu-id="bb2af-242">Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="bb2af-243">**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="bb2af-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="bb2af-244">Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="bb2af-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="bb2af-245">O número máximo de arquivos de despejo na pasta.</span><span class="sxs-lookup"><span data-stu-id="bb2af-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="bb2af-246">Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.</span><span class="sxs-lookup"><span data-stu-id="bb2af-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ Dumptype** ou **LocalDumps do nome do aplicativo de \\ \[ \] \\ decarregamentotype**</span><span class="sxs-lookup"><span data-stu-id="bb2af-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-248">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-248">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-249">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-249">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-250">0-despejo personalizado</span><span class="sxs-lookup"><span data-stu-id="bb2af-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="bb2af-251">1-minidespejo (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="bb2af-252">2-despejo completo</span><span class="sxs-lookup"><span data-stu-id="bb2af-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="bb2af-253">**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="bb2af-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="bb2af-254">Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="bb2af-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="bb2af-255">O tipo de despejo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-255">The dump type.</span></span>

<span data-ttu-id="bb2af-256">Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.</span><span class="sxs-lookup"><span data-stu-id="bb2af-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\** Nome do **aplicativo CustomDumpFlags ou LocalDumps \\ \[ \] \\ CustomDumpFlags**</span><span class="sxs-lookup"><span data-stu-id="bb2af-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-258">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-258">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-259">Um ou mais valores da enumeração [**de \_ tipo de minidespejo**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="bb2af-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="bb2af-260">O padrão é {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.</span><span class="sxs-lookup"><span data-stu-id="bb2af-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="bb2af-261">**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="bb2af-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="bb2af-262">Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="bb2af-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="bb2af-263">As opções de despejo personalizado a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="bb2af-263">The custom dump options to be used.</span></span> <span data-ttu-id="bb2af-264">Esse valor é usado somente quando **dumptype** é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="bb2af-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="bb2af-265">Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.</span><span class="sxs-lookup"><span data-stu-id="bb2af-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span><span class="sxs-lookup"><span data-stu-id="bb2af-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-267">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-267">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-268">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="bb2af-268">Possible values:</span></span><dl> <dd><span data-ttu-id="bb2af-269">0 – habilitado (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2af-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="bb2af-270">1 – desabilitado</span><span class="sxs-lookup"><span data-stu-id="bb2af-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="bb2af-271">Habilitar ou desabilitar o registro em log</span><span class="sxs-lookup"><span data-stu-id="bb2af-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span><span class="sxs-lookup"><span data-stu-id="bb2af-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-273">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-273">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-274">Intervalo de valores possíveis: 1 a 5.000.</span><span class="sxs-lookup"><span data-stu-id="bb2af-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="bb2af-275">O padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="bb2af-275">The default is 1000.</span></span>

<span data-ttu-id="bb2af-276">Tamanho máximo do arquivo morto, em arquivos</span><span class="sxs-lookup"><span data-stu-id="bb2af-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span><span class="sxs-lookup"><span data-stu-id="bb2af-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-278">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-278">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-279">Intervalo de valores possíveis: 1 a 500.</span><span class="sxs-lookup"><span data-stu-id="bb2af-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="bb2af-280">O padrão é 50.</span><span class="sxs-lookup"><span data-stu-id="bb2af-280">The default is 50.</span></span>

<span data-ttu-id="bb2af-281">Tamanho máximo da fila</span><span class="sxs-lookup"><span data-stu-id="bb2af-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span><span class="sxs-lookup"><span data-stu-id="bb2af-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-283">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-283">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-284">Número de dias</span><span class="sxs-lookup"><span data-stu-id="bb2af-284">Number of days</span></span>

<span data-ttu-id="bb2af-285">Intervalo entre lembretes ao usuário para verificar se há soluções, em dias</span><span class="sxs-lookup"><span data-stu-id="bb2af-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nome do pwszOutOfProcessCallbackDll incluindo caminho\]**</span><span class="sxs-lookup"><span data-stu-id="bb2af-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-287">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-287">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-288">O conteúdo do valor é ignorado.</span><span class="sxs-lookup"><span data-stu-id="bb2af-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="bb2af-289">O nome do valor é usado para buscar o valor de pwszOutOfProcessCallbackDll.</span><span class="sxs-lookup"><span data-stu-id="bb2af-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="bb2af-290">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor de registro.</span><span class="sxs-lookup"><span data-stu-id="bb2af-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="bb2af-291">Configurações de relatórios de kernel do WER Live</span><span class="sxs-lookup"><span data-stu-id="bb2af-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="bb2af-292">As configurações de relatórios do kernel ao vivo do WER, que são descritas a seguir, estão localizadas na seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="bb2af-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="bb2af-293">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="bb2af-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="bb2af-294">Subchave FullLiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="bb2af-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="bb2af-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="bb2af-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-296">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-296">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-297">O limite (em horas) de com que frequência qualquer único componente pode criar um despejo ao vivo completo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="bb2af-298">Esse valor deve ser maior ou igual a **SystemThrottleThreshold**.</span><span class="sxs-lookup"><span data-stu-id="bb2af-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="bb2af-299">A definição de ambas como zero (0) desabilitará toda a limitação baseada em tempo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="bb2af-300">O padrão é 168 (7 dias).</span><span class="sxs-lookup"><span data-stu-id="bb2af-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span><span class="sxs-lookup"><span data-stu-id="bb2af-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-302">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-302">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-303">O número máximo de despejos ao vivo completos que podem estar no disco em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="bb2af-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="bb2af-304">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="bb2af-304">The default is 1.</span></span> <span data-ttu-id="bb2af-305">Definir esse valor como zero (0) desativará o recurso de despejo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="bb2af-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span><span class="sxs-lookup"><span data-stu-id="bb2af-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-307">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-307">**REG\_QWORD**</span></span>

<span data-ttu-id="bb2af-308">Um [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que indica o último tempo de relatório ao vivo completo, para o sistema ou um reportType específico.</span><span class="sxs-lookup"><span data-stu-id="bb2af-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="bb2af-309">Isso é usado para calcular se um limite de política foi atendido.</span><span class="sxs-lookup"><span data-stu-id="bb2af-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="bb2af-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="bb2af-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-311">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb2af-311">**REG\_DWORD**</span></span>

<span data-ttu-id="bb2af-312">O limite (em horas) de quantas vezes qualquer componente no sistema pode criar um despejo ao vivo completo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="bb2af-313">O padrão é 120 (5 dias).</span><span class="sxs-lookup"><span data-stu-id="bb2af-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="bb2af-314">Subchave LiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="bb2af-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="bb2af-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span><span class="sxs-lookup"><span data-stu-id="bb2af-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="bb2af-316">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="bb2af-316">**REG\_SZ**</span></span>


<span data-ttu-id="bb2af-317">O local de armazenamento Redirecionado de relatórios de kernel ao vivo.</span><span class="sxs-lookup"><span data-stu-id="bb2af-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="bb2af-318">O local padrão é%systemroot%\LiveKernelReports.</span><span class="sxs-lookup"><span data-stu-id="bb2af-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="bb2af-319">Esse valor deve ser um caminho válido.</span><span class="sxs-lookup"><span data-stu-id="bb2af-319">This value must be a valid path.</span></span> <span data-ttu-id="bb2af-320">O caminho deve estar no formato NT Path.</span><span class="sxs-lookup"><span data-stu-id="bb2af-320">The path must be in NT path format.</span></span> <span data-ttu-id="bb2af-321">Por exemplo, \? ? \c: \LiveDumpsFolder.</span><span class="sxs-lookup"><span data-stu-id="bb2af-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="bb2af-322">Para obter mais informações sobre formatos de caminho, consulte  [formatos de caminho de arquivo em sistemas Windows](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="bb2af-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bb2af-323">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb2af-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb2af-324">Referência do WER</span><span class="sxs-lookup"><span data-stu-id="bb2af-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
