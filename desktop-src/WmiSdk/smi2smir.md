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
# <a name="smi2smir"></a>smi2smir

O compilador SNMP é executado como um único arquivo executável no modo de linha de comando. O compilador aceita um módulo de informações SNMP como entrada e aceita os módulos adicionais necessários para resolver referências externas. Use um dos exemplos de sintaxe de linha de comando a seguir.

Para obter mais informações sobre quando esse compilador é usado, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Comutadores

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de diagnóstico.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _nível de diagnóstico_*_>_*
</dt> <dd>

Tipo de diagnóstico a ser exibido. O padrão é 2.

A seguir está uma lista dos valores de nível de diagnóstico que podem ser definidos:

-   0 = silencioso
-   1 = fatal
-   2 = fatal e aviso
-   3 = mensagens fatais, de aviso e de informações

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _contagem_ de *_>_*
</dt> <dd>

Número máximo de mensagens fatais e de aviso a serem exibidas; a *contagem* deve ser um inteiro decimal positivo. Se **/c** não for especificado, não haverá nenhum limite para o número de erros que podem ser relatados.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de versão.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Especifica a conformidade estrita com a SMI do SNMPv1. O compilador relatará um erro se detectar instruções não SNMPv1.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Especifica a conformidade estrita com o SMI do SNMPv2. O compilador relatará um erro se detectar instruções não SNMPv2.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de comando.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Exclui o módulo especificado do SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Exclui todos os módulos no SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Lista todos os módulos no SMIR.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Executa uma verificação de sintaxe local no módulo.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Executa verificações locais e externas no módulo.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*
</dt> <dd>

Executa verificações locais e externas e carrega o módulo no SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /SA <** _CommandModifier_*_>\]_*
</dt> <dd>

O mesmo que **/a**, mas funciona silenciosamente.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*
</dt> <dd>

Gera um arquivo SMIR. MOF que você pode carregar posteriormente no WMI usando o compilador MOF. Usado pelo provedor de classe SNMP para fornecer classes dinamicamente a um ou mais namespaces. Use essa opção quando você não souber quais MIBs são compatíveis com os dispositivos SNMP que estão sendo gerenciados. O provedor de classe SNMP verifica o dispositivo em tempo de execução para a presença dessa MIB e fornece as classes dinamicamente para o namespace.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*
</dt> <dd>

Gera um arquivo. mof estático que pode ser carregado posteriormente no WMI como classes estáticas para um namespace específico. Use essa opção quando você souber quais MIBs são compatíveis com os dispositivos SNMP que estão sendo gerenciados. Você pode definir o arquivo. mof a ser gerado direcionando a saída do comando para um arquivo especificado. Não use with **/ext/o**.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

O compilador aceita os seguintes modificadores de comando.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Directory_*_>_*
</dt> <dd>

Especifica um diretório a ser procurado pelos módulos MIB dependentes. Use com **/a**, **/EC**, **/g**, **/GC** e **/SA**. A opção **/i** pode aparecer várias vezes no comando; os diretórios são pesquisados na ordem especificada no comando.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/CH**
</dt> <dd>

Gera informações de contexto, como data, hora, host ou usuário, no cabeçalho do arquivo MOF. Use with **/g** e **/GC**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Gera classes [SnmpNotification](snmpnotification.md) . Use com **/a**, **/g** e **/SA**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Gera classes [SnmpExtendedNotification](snmpextendednotification.md) . Use com **/a**, **/g** e **/SA**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Gera somente classes [SnmpNotification](snmpnotification.md) . Use com **/a**, **/g** e **/SA**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Gera somente classes [SnmpExtendedNotification](snmpextendednotification.md) . Use com **/a**, **/g** e **/SA**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

Não mapeia o texto da cláusula de descrição. Use com **/a**, **/g**, **/GC** e **/SA**. Use essa opção quando desejar minimizar os requisitos de armazenamento.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

Recria a tabela de pesquisa MIB antes de concluir a <*CommandArg*> switch. Use com **/a**, **/EC**, **/g** e **/GC**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de registro.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Adiciona o diretório especificado ao registro. O padrão é o diretório atual.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/pd**
</dt> <dd>

Exclui o diretório especificado do registro. O padrão é o diretório atual.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Lista os diretórios de pesquisa MIB no registro.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Recria a tabela de pesquisa de MIB inteira.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de informações do módulo.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**opção**
</dt> <dd>

Retorna o nome ASN. 1 do módulo especificado.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Retorna os nomes ASN. 1 de todos os módulos de importação referenciados pelo módulo de entrada.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

O compilador aceita os seguintes argumentos de ajuda.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Exibe a ajuda sobre a sintaxe do compilador SNMP.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Exibe a ajuda sobre a sintaxe do compilador SNMP.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os módulos de informações de SNMP são gravados em um subconjunto da presintaxe predefinida (ASN. 1) o compilador executa as seguintes funções:

-   Carrega os dados do módulo de informações SNMP.
-   Executa operações de verificação no módulo de informações. Por exemplo, ele verifica a sintaxe local e verifica as referências externas em relação às informações nos módulos subsidiários.
-   Remove todos os dados previamente carregados do SMIR ou remove os dados carregados de um módulo de informação.
-   Retorna o nome do módulo ASN. 1 de um arquivo especificado ou retorna os nomes de módulo ASN. 1 de todos os módulos importados em um arquivo especificado.
-   Retorna os nomes do módulo ASN.1 de todos os módulos de informação do SNMP atualmente carregados no SMIR.
-   Executa a resolução automática de módulos importados em vez de exigir que os usuários especifiquem os módulos necessários manualmente.
-   Executa um modo de carregamento silencioso de operação que não gera nenhuma saída, mas pode ser usado para carregar dados no SMIR durante uma operação de instalação.
-   Gera os dados do módulo informações SNMP no SMIR.
-   Opcionalmente, cria um arquivo MOF estático ou SMIR que contém a saída do módulo de informações.

    Se necessário, você pode carregar o arquivo. mof estático em um namespace WMI. Um arquivo SMIR. mof contém o nome do namespace SNMP no qual as classes devem residir.

## <a name="examples"></a>Exemplos

O exemplo a seguir define o arquivo pra. mof como a saída do arquivo pra. MIB.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens de erro do compilador SNMP](snmp-compiler-error-messages.md)
</dt> <dt>

[Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[Acessando dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 




