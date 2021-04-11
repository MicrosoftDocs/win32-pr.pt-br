---
description: O compilador SNMP é executado como um único arquivo executável no modo de linha de comando.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171795"
---
# <a name="smi2smir"></a><span data-ttu-id="2e391-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="2e391-103">smi2smir</span></span>

<span data-ttu-id="2e391-104">O compilador SNMP é executado como um único arquivo executável no modo de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2e391-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="2e391-105">O compilador aceita um módulo de informações SNMP como entrada e aceita os módulos adicionais necessários para resolver referências externas.</span><span class="sxs-lookup"><span data-stu-id="2e391-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="2e391-106">Use um dos exemplos de sintaxe de linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e391-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="2e391-107">Para obter mais informações sobre quando esse compilador é usado, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2e391-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="2e391-108">Comutadores</span><span class="sxs-lookup"><span data-stu-id="2e391-108">Switches</span></span>

<dl> <span data-ttu-id="2e391-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-110">O compilador aceita os seguintes argumentos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="2e391-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _nível de diagnóstico_*_>_*</span><span class="sxs-lookup"><span data-stu-id="2e391-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-112">Tipo de diagnóstico a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="2e391-112">Type of diagnostics to display.</span></span> <span data-ttu-id="2e391-113">O padrão é 2.</span><span class="sxs-lookup"><span data-stu-id="2e391-113">The default is 2.</span></span>

<span data-ttu-id="2e391-114">A seguir está uma lista dos valores de nível de diagnóstico que podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="2e391-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="2e391-115">0 = silencioso</span><span class="sxs-lookup"><span data-stu-id="2e391-115">0 = Silent</span></span>
-   <span data-ttu-id="2e391-116">1 = fatal</span><span class="sxs-lookup"><span data-stu-id="2e391-116">1 = Fatal</span></span>
-   <span data-ttu-id="2e391-117">2 = fatal e aviso</span><span class="sxs-lookup"><span data-stu-id="2e391-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="2e391-118">3 = mensagens fatais, de aviso e de informações</span><span class="sxs-lookup"><span data-stu-id="2e391-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="2e391-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _contagem_ de *_>_*</span><span class="sxs-lookup"><span data-stu-id="2e391-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-120">Número máximo de mensagens fatais e de aviso a serem exibidas; a *contagem* deve ser um inteiro decimal positivo.</span><span class="sxs-lookup"><span data-stu-id="2e391-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="2e391-121">Se **/c** não for especificado, não haverá nenhum limite para o número de erros que podem ser relatados.</span><span class="sxs-lookup"><span data-stu-id="2e391-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="2e391-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-123">O compilador aceita os seguintes argumentos de versão.</span><span class="sxs-lookup"><span data-stu-id="2e391-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="2e391-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-125">Especifica a conformidade estrita com a SMI do SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="2e391-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="2e391-126">O compilador relatará um erro se detectar instruções não SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="2e391-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="2e391-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-128">Especifica a conformidade estrita com o SMI do SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="2e391-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="2e391-129">O compilador relatará um erro se detectar instruções não SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="2e391-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="2e391-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-131">O compilador aceita os seguintes argumentos de comando.</span><span class="sxs-lookup"><span data-stu-id="2e391-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="2e391-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-133">Exclui o módulo especificado do SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="2e391-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-135">Exclui todos os módulos no SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="2e391-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-137">Lista todos os módulos no SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="2e391-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-139">Executa uma verificação de sintaxe local no módulo.</span><span class="sxs-lookup"><span data-stu-id="2e391-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="2e391-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-141">Executa verificações locais e externas no módulo.</span><span class="sxs-lookup"><span data-stu-id="2e391-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="2e391-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-143">Executa verificações locais e externas e carrega o módulo no SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /SA <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="2e391-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-145">O mesmo que **/a**, mas funciona silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="2e391-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="2e391-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-147">Gera um arquivo SMIR. MOF que você pode carregar posteriormente no WMI usando o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="2e391-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="2e391-148">Usado pelo provedor de classe SNMP para fornecer classes dinamicamente a um ou mais namespaces.</span><span class="sxs-lookup"><span data-stu-id="2e391-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="2e391-149">Use essa opção quando você não souber quais MIBs são compatíveis com os dispositivos SNMP que estão sendo gerenciados.</span><span class="sxs-lookup"><span data-stu-id="2e391-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="2e391-150">O provedor de classe SNMP verifica o dispositivo em tempo de execução para a presença dessa MIB e fornece as classes dinamicamente para o namespace.</span><span class="sxs-lookup"><span data-stu-id="2e391-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="2e391-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-152">Gera um arquivo. mof estático que pode ser carregado posteriormente no WMI como classes estáticas para um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="2e391-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="2e391-153">Use essa opção quando você souber quais MIBs são compatíveis com os dispositivos SNMP que estão sendo gerenciados.</span><span class="sxs-lookup"><span data-stu-id="2e391-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="2e391-154">Você pode definir o arquivo. mof a ser gerado direcionando a saída do comando para um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e391-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="2e391-155">Não use with **/ext/o**.</span><span class="sxs-lookup"><span data-stu-id="2e391-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="2e391-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-157">O compilador aceita os seguintes modificadores de comando.</span><span class="sxs-lookup"><span data-stu-id="2e391-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Directory_*_>_*</span><span class="sxs-lookup"><span data-stu-id="2e391-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="2e391-159">Especifica um diretório a ser procurado pelos módulos MIB dependentes.</span><span class="sxs-lookup"><span data-stu-id="2e391-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="2e391-160">Use com **/a**, **/EC**, **/g**, **/GC** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="2e391-161">A opção **/i** pode aparecer várias vezes no comando; os diretórios são pesquisados na ordem especificada no comando.</span><span class="sxs-lookup"><span data-stu-id="2e391-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-162"><span id="_ch"></span><span id="_CH"></span>**/CH**</span><span class="sxs-lookup"><span data-stu-id="2e391-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-163">Gera informações de contexto, como data, hora, host ou usuário, no cabeçalho do arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="2e391-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="2e391-164">Use with **/g** e **/GC**.</span><span class="sxs-lookup"><span data-stu-id="2e391-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-165"><span id="_t"></span><span id="_T"></span>**/t**</span><span class="sxs-lookup"><span data-stu-id="2e391-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-166">Gera classes [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2e391-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="2e391-167">Use com **/a**, **/g** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span><span class="sxs-lookup"><span data-stu-id="2e391-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-169">Gera classes [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2e391-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="2e391-170">Use com **/a**, **/g** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="2e391-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-172">Gera somente classes [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2e391-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="2e391-173">Use com **/a**, **/g** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="2e391-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-175">Gera somente classes [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2e391-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="2e391-176">Use com **/a**, **/g** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-177"><span id="_s"></span><span id="_S"></span>**/s**</span><span class="sxs-lookup"><span data-stu-id="2e391-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-178">Não mapeia o texto da cláusula de descrição.</span><span class="sxs-lookup"><span data-stu-id="2e391-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="2e391-179">Use com **/a**, **/g**, **/GC** e **/SA**.</span><span class="sxs-lookup"><span data-stu-id="2e391-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="2e391-180">Use essa opção quando desejar minimizar os requisitos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2e391-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span><span class="sxs-lookup"><span data-stu-id="2e391-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-182">Recria a tabela de pesquisa MIB antes de concluir a <*CommandArg*> switch.</span><span class="sxs-lookup"><span data-stu-id="2e391-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="2e391-183">Use com **/a**, **/EC**, **/g** e **/GC**.</span><span class="sxs-lookup"><span data-stu-id="2e391-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="2e391-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-185">O compilador aceita os seguintes argumentos de registro.</span><span class="sxs-lookup"><span data-stu-id="2e391-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span><span class="sxs-lookup"><span data-stu-id="2e391-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-187">Adiciona o diretório especificado ao registro.</span><span class="sxs-lookup"><span data-stu-id="2e391-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="2e391-188">O padrão é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="2e391-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span><span class="sxs-lookup"><span data-stu-id="2e391-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-190">Exclui o diretório especificado do registro.</span><span class="sxs-lookup"><span data-stu-id="2e391-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="2e391-191">O padrão é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="2e391-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span><span class="sxs-lookup"><span data-stu-id="2e391-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-193">Lista os diretórios de pesquisa MIB no registro.</span><span class="sxs-lookup"><span data-stu-id="2e391-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="2e391-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-195">Recria a tabela de pesquisa de MIB inteira.</span><span class="sxs-lookup"><span data-stu-id="2e391-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="2e391-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-197">O compilador aceita os seguintes argumentos de informações do módulo.</span><span class="sxs-lookup"><span data-stu-id="2e391-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-198"><span id="_n"></span><span id="_N"></span>**opção**</span><span class="sxs-lookup"><span data-stu-id="2e391-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-199">Retorna o nome ASN. 1 do módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e391-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="2e391-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-201">Retorna os nomes ASN. 1 de todos os módulos de importação referenciados pelo módulo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e391-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="2e391-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="2e391-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="2e391-203">O compilador aceita os seguintes argumentos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="2e391-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="2e391-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-205">Exibe a ajuda sobre a sintaxe do compilador SNMP.</span><span class="sxs-lookup"><span data-stu-id="2e391-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="2e391-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="2e391-207">Exibe a ajuda sobre a sintaxe do compilador SNMP.</span><span class="sxs-lookup"><span data-stu-id="2e391-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e391-208">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e391-208">Remarks</span></span>

<span data-ttu-id="2e391-209">Os módulos de informações de SNMP são gravados em um subconjunto da presintaxe predefinida (ASN. 1) o compilador executa as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="2e391-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="2e391-210">Carrega os dados do módulo de informações SNMP.</span><span class="sxs-lookup"><span data-stu-id="2e391-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="2e391-211">Executa operações de verificação no módulo de informações.</span><span class="sxs-lookup"><span data-stu-id="2e391-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="2e391-212">Por exemplo, ele verifica a sintaxe local e verifica as referências externas em relação às informações nos módulos subsidiários.</span><span class="sxs-lookup"><span data-stu-id="2e391-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="2e391-213">Remove todos os dados previamente carregados do SMIR ou remove os dados carregados de um módulo de informação.</span><span class="sxs-lookup"><span data-stu-id="2e391-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="2e391-214">Retorna o nome do módulo ASN. 1 de um arquivo especificado ou retorna os nomes de módulo ASN. 1 de todos os módulos importados em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e391-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="2e391-215">Retorna os nomes do módulo ASN.1 de todos os módulos de informação do SNMP atualmente carregados no SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="2e391-216">Executa a resolução automática de módulos importados em vez de exigir que os usuários especifiquem os módulos necessários manualmente.</span><span class="sxs-lookup"><span data-stu-id="2e391-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="2e391-217">Executa um modo de carregamento silencioso de operação que não gera nenhuma saída, mas pode ser usado para carregar dados no SMIR durante uma operação de instalação.</span><span class="sxs-lookup"><span data-stu-id="2e391-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="2e391-218">Gera os dados do módulo informações SNMP no SMIR.</span><span class="sxs-lookup"><span data-stu-id="2e391-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="2e391-219">Opcionalmente, cria um arquivo MOF estático ou SMIR que contém a saída do módulo de informações.</span><span class="sxs-lookup"><span data-stu-id="2e391-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="2e391-220">Se necessário, você pode carregar o arquivo. mof estático em um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="2e391-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="2e391-221">Um arquivo SMIR. mof contém o nome do namespace SNMP no qual as classes devem residir.</span><span class="sxs-lookup"><span data-stu-id="2e391-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="2e391-222">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e391-222">Examples</span></span>

<span data-ttu-id="2e391-223">O exemplo a seguir define o arquivo pra. mof como a saída do arquivo pra. MIB.</span><span class="sxs-lookup"><span data-stu-id="2e391-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="2e391-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e391-224">Requirements</span></span>



| <span data-ttu-id="2e391-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e391-225">Requirement</span></span> | <span data-ttu-id="2e391-226">Valor</span><span class="sxs-lookup"><span data-stu-id="2e391-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2e391-227">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e391-227">Minimum supported client</span></span><br/> | <span data-ttu-id="2e391-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e391-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2e391-229">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e391-229">Minimum supported server</span></span><br/> | <span data-ttu-id="2e391-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e391-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e391-231">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e391-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e391-232">Mensagens de erro do compilador SNMP</span><span class="sxs-lookup"><span data-stu-id="2e391-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="2e391-233">Configurando o ambiente SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="2e391-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="2e391-234">Acessando dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="2e391-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




