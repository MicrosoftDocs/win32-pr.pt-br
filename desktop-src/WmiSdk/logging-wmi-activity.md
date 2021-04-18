---
description: Não há mais suporte para os arquivos de log do WMI.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrando em log a atividade WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781354"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="aee1f-103">Registrando em log a atividade WMI</span><span class="sxs-lookup"><span data-stu-id="aee1f-103">Logging WMI Activity</span></span>

<span data-ttu-id="aee1f-104">Não há mais suporte para os arquivos de log do WMI.</span><span class="sxs-lookup"><span data-stu-id="aee1f-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="aee1f-105">A partir do Windows Vista, o WMI usa o [ETW (rastreamento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal)) e eventos que estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="aee1f-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="aee1f-106">Para obter mais informações, consulte o provedor de ETW e a documentação de linha de comando do [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="aee1f-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="aee1f-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="aee1f-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="aee1f-108">Arquivos de log do WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="aee1f-109">Atividades de registro em log para componentes básicos do WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="aee1f-110">Atividades de registro em log para componentes do provedor de WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="aee1f-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aee1f-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="aee1f-112">Arquivos de log do WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="aee1f-113">Os arquivos de log criados pelo WMI e vários provedores registram: eventos, rastreamento ou dados de diagnóstico, erros e várias atividades.</span><span class="sxs-lookup"><span data-stu-id="aee1f-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="aee1f-114">Somente os administradores têm acesso de leitura à pasta de log do WMI encontrada em% windir% \\ System32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="aee1f-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="aee1f-115">Somente os componentes principais do WMI ou os provedores WMI gravam em arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="aee1f-116">Você só pode ler ou exibir os dados nesses logs para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="aee1f-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="aee1f-117">Você pode criar e armazenar seus próprios arquivos de log no diretório de log do WMI.</span><span class="sxs-lookup"><span data-stu-id="aee1f-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="aee1f-118">Atividades de registro em log para componentes básicos do WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="aee1f-119">Esses arquivos não contêm um formato consistente que seja adequado para leitura programaticamente.</span><span class="sxs-lookup"><span data-stu-id="aee1f-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="aee1f-120">Para obter mais informações sobre logs específicos, consulte [arquivos de log do WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="aee1f-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="aee1f-121">As atividades de registro em log para componentes principais do WMI ocorrem quando as seguintes chaves do registro são definidas:</span><span class="sxs-lookup"><span data-stu-id="aee1f-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="aee1f-122">Nível de log</span><span class="sxs-lookup"><span data-stu-id="aee1f-122">Logging level</span></span>

    <span data-ttu-id="aee1f-123">As alterações no valor do registro de nível de log entram em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="aee1f-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="aee1f-124">Nenhuma reinicialização do serviço WMI é necessária.</span><span class="sxs-lookup"><span data-stu-id="aee1f-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="aee1f-125">**HKEY \_ SOFTWARE do \_ computador local** \\  \\ registro em log **do Microsoft** \\ **WBEM** \\ **CIMOM** \\  = 2</span><span class="sxs-lookup"><span data-stu-id="aee1f-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="aee1f-126">A lista a seguir lista os níveis de log que podem ser definidos no registro.</span><span class="sxs-lookup"><span data-stu-id="aee1f-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="aee1f-127">Nível de log</span><span class="sxs-lookup"><span data-stu-id="aee1f-127">Logging level</span></span> | <span data-ttu-id="aee1f-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="aee1f-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="aee1f-129">0</span><span class="sxs-lookup"><span data-stu-id="aee1f-129">0</span></span>             | <span data-ttu-id="aee1f-130">Sem registro em log</span><span class="sxs-lookup"><span data-stu-id="aee1f-130">No Logging</span></span>                |
    | <span data-ttu-id="aee1f-131">1</span><span class="sxs-lookup"><span data-stu-id="aee1f-131">1</span></span>             | <span data-ttu-id="aee1f-132">Erros de log apenas</span><span class="sxs-lookup"><span data-stu-id="aee1f-132">Log only errors</span></span>           |
    | <span data-ttu-id="aee1f-133">2</span><span class="sxs-lookup"><span data-stu-id="aee1f-133">2</span></span>             | <span data-ttu-id="aee1f-134">Log detalhado (padrão)</span><span class="sxs-lookup"><span data-stu-id="aee1f-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="aee1f-135">Local do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="aee1f-135">Log file location</span></span>

    <span data-ttu-id="aee1f-136">Para que as alterações no local do arquivo de log entrem em vigor, reinicie o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="aee1f-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="aee1f-137">**HKEY \_ \_** Diretório de log do software do computador local \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Directory** =% windir% \\ System32 \\ WBEM \\ logs</span><span class="sxs-lookup"><span data-stu-id="aee1f-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="aee1f-138">Tamanho máximo do arquivo de log, em bytes</span><span class="sxs-lookup"><span data-stu-id="aee1f-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="aee1f-139">**HKEY \_ \_Computador local** \\ **software** \\ arquivo de log **do Microsoft** \\ **WBEM** \\ **CIMOM** \\ **tamanho máximo** = 65536</span><span class="sxs-lookup"><span data-stu-id="aee1f-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="aee1f-140">Você pode alterar esses valores de chave do registro por meio do editor do registro ou através do snap-in do WMI para o console de gerenciamento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aee1f-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="aee1f-141">**Para definir o nível de log para WMI antes do Windows Vista**</span><span class="sxs-lookup"><span data-stu-id="aee1f-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="aee1f-142">Clique em **Iniciar** e em **Executar**.</span><span class="sxs-lookup"><span data-stu-id="aee1f-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="aee1f-143">Digite **wmimgmt. msc**</span><span class="sxs-lookup"><span data-stu-id="aee1f-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="aee1f-144">No menu **Ação**, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="aee1f-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="aee1f-145">Na guia **registro em log** , defina o nível de log como **desabilitado**, **habilitado** ou **detalhado**.</span><span class="sxs-lookup"><span data-stu-id="aee1f-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="aee1f-146">Em **local:**, digite o caminho para a pasta do arquivo de log e, em **tamanho máximo (bytes):**, defina o tamanho máximo, em bytes, do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="aee1f-147">Para obter mais informações sobre como definir as propriedades do arquivo de log, consulte a ajuda online para o aplicativo controle WMI.</span><span class="sxs-lookup"><span data-stu-id="aee1f-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="aee1f-148">Atividades de registro em log para componentes do provedor de WMI antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee1f-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="aee1f-149">Quando o registro em log para componentes do WMI Core está habilitado, o log também é habilitado para qualquer provedor com recursos de log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="aee1f-150">A lista a seguir lista os valores necessários.</span><span class="sxs-lookup"><span data-stu-id="aee1f-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="aee1f-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**Grupo**</span><span class="sxs-lookup"><span data-stu-id="aee1f-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="aee1f-152">Caminho completo e nome do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-152">Full path and file name of the log file.</span></span> <span data-ttu-id="aee1f-153">O valor padrão é% windir% \\ System32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="aee1f-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="aee1f-154">O **tipo** nomeado value deve ser definido como = File para que esse valor nomeado seja usado.</span><span class="sxs-lookup"><span data-stu-id="aee1f-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="aee1f-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Geral**</span><span class="sxs-lookup"><span data-stu-id="aee1f-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="aee1f-156">Uma máscara lógica de 32 bits que define o tipo de saída de depuração gerado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="aee1f-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="aee1f-157">Esse valor é dependente do provedor.</span><span class="sxs-lookup"><span data-stu-id="aee1f-157">This value is provider-dependent.</span></span> <span data-ttu-id="aee1f-158">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="aee1f-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="aee1f-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**Cedido**</span><span class="sxs-lookup"><span data-stu-id="aee1f-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="aee1f-160">Tamanho máximo do arquivo, em bytes, do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="aee1f-161">Esse valor inteiro deve estar no intervalo de 1024 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="aee1f-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="aee1f-162">Quando o tamanho do arquivo exceder esse valor, o arquivo será renomeado para **~ filename** e um novo arquivo de log vazio será criado.</span><span class="sxs-lookup"><span data-stu-id="aee1f-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="aee1f-163">O espaço em disco necessário para o arquivo de log é o dobro do valor de **MaxFileSize**.</span><span class="sxs-lookup"><span data-stu-id="aee1f-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="aee1f-164">O valor padrão é 65.535.</span><span class="sxs-lookup"><span data-stu-id="aee1f-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="aee1f-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="aee1f-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="aee1f-166">Pode ser definido como = File ou = Debugger.</span><span class="sxs-lookup"><span data-stu-id="aee1f-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="aee1f-167">Se definido como = File, as informações de rastreamento serão gravadas no arquivo de log especificado no **arquivo** denominado Value.</span><span class="sxs-lookup"><span data-stu-id="aee1f-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="aee1f-168">O valor padrão é = File.</span><span class="sxs-lookup"><span data-stu-id="aee1f-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="aee1f-169">Por exemplo, para registrar consultas e obter chamadas de instância do provedor de exibição, use os valores de chave do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="aee1f-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="aee1f-170">O log estará localizado na pasta de log e será o tamanho de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="aee1f-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="aee1f-171">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Providers** \\ **loggingprovider** \\  \\ **arquivo** = C: \\ Windows \\ System32 \\ WBEM \\ logs \\ viewprovider. log</span><span class="sxs-lookup"><span data-stu-id="aee1f-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="aee1f-172">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **provedores** \\ **logs** \\ **viewprovider** \\ **nível** = 2</span><span class="sxs-lookup"><span data-stu-id="aee1f-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="aee1f-173">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **provedores** \\ **logs** \\ **viewprovider** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="aee1f-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="aee1f-174">**HKEY \_ SOFTWARE da \_ máquina local** \\ **softwares** \\ **Microsoft** \\ **WBEM** \\  \\ **logs** \\ **viewprovider** \\ **tipo** = arquivo</span><span class="sxs-lookup"><span data-stu-id="aee1f-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="aee1f-175">Para seus próprios provedores com recursos de log, você precisa gravar as chaves e os valores necessários do registro para habilitar o registro em log.</span><span class="sxs-lookup"><span data-stu-id="aee1f-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aee1f-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aee1f-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee1f-177">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="aee1f-177">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="aee1f-178">Arquivos de log do WMI</span><span class="sxs-lookup"><span data-stu-id="aee1f-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="aee1f-179">Classes de solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="aee1f-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="aee1f-180">Rastreando a atividade WMI</span><span class="sxs-lookup"><span data-stu-id="aee1f-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
