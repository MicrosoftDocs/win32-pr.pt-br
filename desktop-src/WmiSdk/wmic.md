---
description: O utilitário de linha de comando do WMI (WMIC) fornece uma interface de linha de comando para o WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222924"
---
# <a name="wmic"></a>wmic

O utilitário de linha de comando do WMI (WMIC) fornece uma interface de linha de comando para Instrumentação de Gerenciamento do Windows (WMI). O WMIC é compatível com shells e comandos de utilitário existentes. Veja a seguir um tópico de referência geral para o WMIC. Para obter mais informações e diretrizes sobre como usar o WMIC, incluindo informações adicionais sobre aliases, verbos, switches e comandos, consulte [usando instrumentação de gerenciamento do Windows linha de comando](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) e [WMIC – use o controle de linha de comando sobre o WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Um alias é uma renomeação amigável de uma classe, propriedade ou método que torna o WMI mais fácil de usar e ler. Você pode determinar quais aliases estão disponíveis para WMIC por meio do **/?** . Você também pode determinar os aliases para uma classe específica usando o **<className> /?** . Para obter mais informações, consulte [aliases do WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Comutador

Um comutador é uma opção WMIC que pode ser definida globalmente ou opcionalmente. Para obter uma lista de opções disponíveis, consulte [Opções de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbos

Para usar verbos no WMIC, insira o nome do alias seguido pelo verbo. Se um alias não oferecer suporte a um verbo, você receberá a mensagem "o provedor não é capaz da operação tentada". Para obter mais informações, consulte [verbos do WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

A maioria dos aliases dá suporte aos verbos a seguir.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>ASSOCIAÇÕES
</dt> <dd>

Retorna o resultado da `Associators of (<wmi_object>)` consulta em que *<\_ objeto WMI>* é o caminho dos objetos retornados pelos comandos de **classe** ou **caminho** . Os resultados são instâncias associadas ao objeto. Quando ASSOC é usado com um alias, as classes com a classe subjacente ao alias são retornadas. Por padrão, a saída é retornada no formato HTML.

O verbo ASSOC tem as seguintes opções.



| Opção                         | Descrição                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Os pontos de extremidade retornados associados ao objeto de origem devem pertencer ou derivar da classe especificada.      |
| /RESULTROLE:<rolename>   | Os pontos de extremidade retornados devem reproduzir uma função específica em associações com o objeto de origem.                              |
| /ASSOCCLASS:<assocclass> | Os pontos de extremidade retornados devem ser associados à origem por meio da classe especificada ou de uma de suas classes derivadas. |



 

Exemplo: **assoc. do sistema operacional**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>LIGAÇÃO
</dt> <dd>

Executa um método.

Exemplo: **serviço em que Caption = ' telnet ' chama STARTSERVICE**

> [!Note]  
> Para determinar os métodos disponíveis para uma determinada classe, use **/?**. Por exemplo, **serviço em que Caption = "Telnet" Call/?** lista as funções disponíveis para a classe de serviço.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>CRIADA
</dt> <dd>

Cria uma nova instância e define os valores de propriedade. CREATE não pode ser usado para criar uma nova classe.

Exemplo: **ambiente Create Name = "Temp"; VARIABLEVALUE = "NEW"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>APAGAR
</dt> <dd>

Exclui a instância atual ou o conjunto de instâncias. DELETE pode ser usado para excluir uma classe.

Exemplo: **processo em que Name = "CALC.EXE" Delete**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Obter
</dt> <dd>

Recuperar valores de propriedade específicos.

GET tem as seguintes opções.



| Opção                               | Descrição                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | A saída é formatada com cada valor listado em uma linha separada e com o nome da propriedade.                                           |
| /ALL                                 | A saída é formatada como uma tabela.                                                                                                            |
| Vertida<translation table> | Traduza a saída usando a tabela de conversão chamada pelo comando. As tabelas de tradução BasicXml e novírgula estão incluídas com a WMIC. |
| Cada<interval>              | Repita o comando a cada <interval> segundos.                                                                                         |
| Ao<format specifier>     | Especifica um nome de arquivo de palavra-chave ou XSL para formatar os dados.                                                                                  |



 

Exemplo: **processar Get Name**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>LISTA
</dt> <dd>

Mostra os dados. LIST é o verbo padrão.

A lista tem os seguintes advérbios.



| Advérbio   | Descrição                                                  |
|----------|--------------------------------------------------------------|
| RESUMIDO    | Conjunto principal das propriedades.                                  |
| FULL     | Conjunto completo de propriedades. Esse é o advérbio padrão para a lista. |
| INSTANCE | Somente caminhos de instância.                                         |
| STATUS   | Status dos objetos.                                       |
| SYSTEM   | Propriedades de sistema.                                           |



 

A lista tem as seguintes opções.



| Opção                               | Descrição                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Vertida<translation table> | Traduza a saída usando a tabela de conversão chamada pelo comando. As tabelas de tradução BasicXml e novírgula estão incluídas com a WMIC. |
| Cada<interval>              | Repita o comando a cada <interval> segundos.                                                                                         |
| Ao<format specifier>     | Especifica um nome de arquivo de palavra-chave ou XSL para formatar os dados.                                                                                  |



 

Exemplo: **Resumo da lista de processos**

</dd> <dt>

<span id="SET"></span><span id="set"></span>Definição
</dt> <dd>

Atribui valores a propriedades. Exemplo: **ambiente Set Name = "Temp"**, **VARIABLEVALUE = "New"**

</dd> </dl>

## <a name="switches"></a>Comutadores

Opções globais são usadas para definir padrões para o ambiente do WMIC. Você pode exibir o valor atual das condições definidas por essas opções inserindo o comando de **contexto** .

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Namespace que o alias usa normalmente. O padrão é raiz \\ cimv2.

Exemplo: **/namespace: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

O namespace WMIC normalmente procura aliases e outras informações de WMIC.

Exemplo: **/Role: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Nomes de computador, delimitado por vírgulas. Todos os comandos são executados de forma síncrona em todos os computadores listados nesse valor. Os nomes de arquivo devem ser prefixados com &. Os nomes de computador dentro de um arquivo devem ser delimitados por vírgula ou em linhas separadas.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Nível de representação.

Exemplo: **/IMPLEVEL: Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Nível de autenticação.

Exemplo: **/AUTHLEVEL: PKT**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Localidade.

Exemplo: **/locale: MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Habilitar ou desabilitar todos os privilégios.

Exemplo: **/Privileges: Enable** ou **/Privileges: Disable**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Exiba o êxito ou a falha de todas as funções usadas para executar comandos WMIC.

Exemplo: **/trace: on** ou **/trace: off**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Registra todas as saídas em um arquivo XML. A saída também é exibida no prompt de comando.

Exemplo: **/Record:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

Normalmente, os comandos DELETE são confirmados.

Exemplo: **/Interactive: on** ou **/Interactive: off**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Se estiver executando ping nos computadores/NODE antes de enviar comandos WMIC para eles. Se um computador não responder, os comandos WMIC não serão enviados a ele.

Exemplo: "/FAILFAST: ON" ou "/FAILFAST: OFF"

**/FAILFAST WMIC: 1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/
</dt> <dd>

Nome de usuário usado pela WMIC ao acessar os computadores ou computadores do/NODE especificados nos aliases. Você receberá uma solicitação de senha. Um nome de usuário não pode ser usado com o computador local.

Exemplo: **/User:**_jsmith_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Senha usada pelo WMIC ao acessar os computadores/NODE. A senha é visível na linha de comando.

Exemplo: **/password:**_senha_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Especifica um modo para todo o redirecionamento de saída. A saída não aparece na linha de comando e o destino é limpo antes do início da saída. Os valores válidos são STDOUT, CLIPBOARD ou um nome de arquivo.

Exemplo: **/output: Clipboard**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Especifica um modo para todo o redirecionamento de saída. A saída não aparece na linha de comando e o destino não é limpo antes do início da saída e a saída é acrescentada ao final do conteúdo atual do destino. Os valores válidos são STDOUT, CLIPBOARD ou um nome de arquivo.

Exemplo: **/Append: Clipboard**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Usado com a **lista** e **obter** a opção/Every. Se a AGREGAção estiver ATIVAda, LISTe e obtenha a exibição dos resultados quando todos os computadores da/NODE tiverem respondido ou atingido o tempo limite. Se a AGREGAção estiver desativada, LISTe e exiba seus resultados assim que eles forem recebidos.

Exemplo: **/Aggregate: off** ou **/Aggregate: on**

</dd> </dl>

## <a name="commands"></a>Comandos

Os comandos WMIC a seguir estão disponíveis o tempo todo. Para obter mais informações, consulte [comandos WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>CLASSES
</dt> <dd>

Escape do modo de alias padrão do WMIC para acessar classes diretamente no esquema do WMI. Para obter mais informações sobre as classes WMI disponíveis, consulte [classes WMI](wmi-classes.md).

Exemplo: **WMIC/output: c: \\ClassOutput.htm classe Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>Multi-Path
</dt> <dd>

Escape do modo de alias padrão do WMIC para acessar instâncias diretamente no esquema do WMI.

Exemplo: **WMIC/output: c: \\PathOutput.txt caminho Win32 \_ SoundDevice get/value**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>NOTICIOSO
</dt> <dd>

Exibe os valores atuais de todas as opções globais.

Exemplo: **contexto WMIC**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>Sai
</dt> <dd>

Sair do WMIC.

Exemplo: **WMIC sair**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>SIDO
</dt> <dd>

Sair do WMIC.

Exemplo: **WMIC sair**

</dd> </dl>

## <a name="examples"></a>Exemplos

O [script para configurar a amostra de IP/sub-rede/gateway/DNS usando WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) na galeria do TechNet descreve como modificar e atualizar as configurações de IP, sub-rede, gateway e DNS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

