---
description: Descreve erros de provedor WMI SNMP de 101 a 110.
ms.assetid: baa64233-eb19-4f52-836b-5bdf4a23ae4f
ms.tgt_platform: multiple
title: Erros de 101 a 110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a33a4bc1aee7d9357c0dd46c7bae2e70390f892
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884402"
---
# <a name="errors-101-through-110"></a>Erros de 101 a 110

Descreve erros de provedor WMI SNMP de 101 a 110.

[Erro fatal 101](#fatal-error-101)

[Erro fatal 102](#fatal-error-102)

[Erro fatal 103](#fatal-error-103)

[Erro fatal 104](#fatal-error-104)

[Erro fatal 105](#fatal-error-105)

[Erro fatal 106](#fatal-error-106)

[Erro fatal 107](#fatal-error-107)

[Erro fatal 108](#fatal-error-108)

[Erro fatal 109](#fatal-error-109)

[Aviso 110](#warning-110)

## <a name="fatal-error-101"></a>Erro fatal 101

<dl> <dt>

<span id="_101__Fatal____Usage_"></span><span id="_101__fatal____usage_"></span><span id="_101__FATAL____USAGE_"></span>**<101, fatal>: "Uso:**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___VersionArgs___CommandArgs_"></span><span id="smi2smir__diagnosticargs___versionargs___commandargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___VERSIONARGS___COMMANDARGS_"></span>**smi2smir &lt; DiagnosticArgs &gt; &lt; &gt; &lt; VersionArgs CommandArgs&gt;**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___RegistryArgs_"></span><span id="smi2smir__diagnosticargs___registryargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___REGISTRYARGS_"></span>**smi2smir &lt; DiagnosticArgs &gt; &lt; RegistryArgs&gt;**
</dt> <dd></dd> <dt>

<span id="smi2smir__HelpArgs__"></span><span id="smi2smir__helpargs__"></span><span id="SMI2SMIR__HELPARGS__"></span>**smi2smir &lt; HelpArgs &gt; "**
</dt> <dd>

Erro de sintaxe de linha de comando. Isso é seguido por uma explicação das opções.

</dd> </dl>

## <a name="fatal-error-102"></a>Erro fatal 102

<dl> <dt>

<span id="_102__Fatal___Invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__fatal___invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__FATAL___INVALID_ARGUMENT_ON_COMMAND_LINE_AFTER__LAST_CORRECT_ARGUMENT__"></span>**<102, Fatal>:"Argumento inválido na linha de comando após <last correct argument> "**
</dt> <dd>

Erro de sintaxe de linha de comando. Há alguns argumentos extras ou uma opção não é válida na linha de comando. O parâmetro refere-se ao último argumento que foi lido corretamente na linha de comando e, possivelmente, pode ser smi2smir, que é o nome do arquivo executável para o compilador de informações do módulo <last correct argument> SNMP.

</dd> </dl>

## <a name="fatal-error-103"></a>Erro fatal 103

<dl> <dt>

<span id="_103__Fatal____Diagnostic_Level_not_specified_for_the__m_switch_"></span><span id="_103__fatal____diagnostic_level_not_specified_for_the__m_switch_"></span><span id="_103__FATAL____DIAGNOSTIC_LEVEL_NOT_SPECIFIED_FOR_THE__M_SWITCH_"></span>**<103, Fatal>: "Nível de diagnóstico não especificado para a opção /m"**
</dt> <dd>

Erro de sintaxe de linha de comando. Se você especificar a **opção /m,** também deverá especificar um nível de diagnóstico de 0, 1 ou 2.

</dd> </dl>

## <a name="fatal-error-104"></a>Erro fatal 104

<dl> <dt>

<span id="_104__Fatal____Diagnostic_Level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__fatal____diagnostic_level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__FATAL____DIAGNOSTIC_LEVEL_MUST_BE_0__1_OR_2_FOR_THE__M_SWITCH_"></span>**<104, fatal>: "O nível de diagnóstico deve ser 0, 1 ou 2 para a opção /m"**
</dt> <dd>

Erro de sintaxe de linha de comando. Se você especificar a **opção /m,** também deverá especificar um nível de diagnóstico de 0, 1 ou 2.

</dd> </dl>

## <a name="fatal-error-105"></a>Erro fatal 105

<dl> <dt>

<span id="_105__Fatal____Maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__fatal____maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__FATAL____MAXIMUM_DIAGNOSTIC_COUNT_MISSING_AFTER_THE__C_SWITCH_"></span>**<105, Fatal>: "Contagem máxima de diagnóstico ausente após a opção /c"**
</dt> <dd>

Erro de sintaxe de linha de comando. Se você especificar a **opção /c,** também deverá especificar um inteiro não negativo como a contagem máxima.

</dd> </dl>

## <a name="fatal-error-106"></a>Erro fatal 106

<dl> <dt>

<span id="_106__Fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__FATAL_____ARGUMENT__IS_NOT_A_VALID_DIAGNOSTIC_COUNT_"></span>**<106, Fatal>: " &lt; o argumento não é uma contagem de diagnóstico &gt; válida"**
</dt> <dd>

Erro de sintaxe de linha de comando. Se você especificar a **opção /c,** também deverá especificar um inteiro não negativo como a contagem máxima.

</dd> </dl>

## <a name="fatal-error-107"></a>Erro fatal 107

<dl> <dt>

<span id="_107__Fatal____File_Name_s__missing_"></span><span id="_107__fatal____file_name_s__missing_"></span><span id="_107__FATAL____FILE_NAME_S__MISSING_"></span>**<107, fatal>: "Nomes de arquivo ausentes"**
</dt> <dd>

Erro semântico de linha de comando. Um ou mais nomes de arquivo devem ser especificados na linha de comando para a combinação de opções especificada.

</dd> </dl>

## <a name="fatal-error-108"></a>Erro fatal 108

<dl> <dt>

<span id="_108__Fatal____No_command_argument_specified_"></span><span id="_108__fatal____no_command_argument_specified_"></span><span id="_108__FATAL____NO_COMMAND_ARGUMENT_SPECIFIED_"></span>**<108, Fatal>: "Nenhum argumento de comando especificado"**
</dt> <dd>

Erro de sintaxe de linha de comando. Alguma ação deve ser especificada na linha de comando.

</dd> </dl>

## <a name="fatal-error-109"></a>Erro fatal 109

<dl> <dt>

<span id="_109__Fatal____Module_name_missing_"></span><span id="_109__fatal____module_name_missing_"></span><span id="_109__FATAL____MODULE_NAME_MISSING_"></span>**<109, Fatal>: "Nome do módulo ausente"**
</dt> <dd>

Erro de sintaxe de linha de comando.

</dd> </dl>

## <a name="warning-110"></a>Aviso 110

<dl> <dt>

<span id="_110__Warning____No_include_path_specified_after_the__i_switch_"></span><span id="_110__warning____no_include_path_specified_after_the__i_switch_"></span><span id="_110__WARNING____NO_INCLUDE_PATH_SPECIFIED_AFTER_THE__I_SWITCH_"></span>**<110, Aviso>: "Nenhum caminho de inclusão especificado após a opção /i"**
</dt> <dd>

Aviso de sintaxe de linha de comando. Se você especificar a **opção /i,** também deverá especificar o caminho para os arquivos incluídos.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



