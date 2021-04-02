---
description: A tabela de componentes lista os componentes e tem as colunas a seguir.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Tabela de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b721996767fa98209f0e13530f8f1bb1ba8cca07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164833"
---
# <a name="component-table"></a>Tabela de componentes

A tabela de componentes lista os componentes e tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente   | [Identificador](identifier.md) | S   | N        |
| ComponentId | [GUID](guid.md)             | N   | S        |
| Diretório\_ | [Identificador](identifier.md) | N   | N        |
| Atributos  | [Inteiro](integer.md)       | N   | N        |
| Condição   | [Condição](condition.md)   | N   | S        |
| KeyPath     | [Identificador](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Identifica o registro do componente.

Chave de tabela primária.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

Um GUID de cadeia de caracteres exclusivo para este componente, versão e idioma.

Observe que as letras dessas GUIDs devem estar em letras maiúsculas. Utilitários como GUIDGEN podem gerar GUIDs contendo letras minúsculas. As letras minúsculas devem ser alteradas para maiúsculas para fazer esses GUIDs de código de componente válidos.

Se essa coluna for nula, o instalador não registrará o componente e o componente não poderá ser removido ou reparado pelo instalador. Isso pode ser intencionalmente feito se o componente só for necessário durante a instalação, como uma ação personalizada que limpa arquivos temporários ou remove um produto antigo. Ele também pode ser útil ao copiar arquivos de dados para um computador do usuário que não precise ser registrado.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

Chave externa de uma entrada na [tabela de diretórios](directory-table.md). Esse é um nome de propriedade cujo valor contém o caminho real, que pode ser definido pela [ação AppSearch](appsearch-action.md) ou com a configuração padrão obtida da tabela de diretório.

Os desenvolvedores devem evitar a criação de componentes que colocam arquivos em uma das pastas de perfil do usuário. Esses arquivos não estarão disponíveis para todos os usuários em situações de vários usuários e poderiam fazer com que o instalador exiba permanentemente o componente, exigindo o reparo.

Chave externa para a coluna um da tabela de diretórios.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta coluna contém um sinalizador de bits que especifica as opções de execução remota. Adicione o bit indicado ao valor total na coluna para incluir uma opção.

> [!Note]  
> No caso de um arquivo. msi que está sendo baixado de um local da Web, os sinalizadores de atributo não devem ser definidos para permitir que um componente seja executado de origem. Essa é uma limitação do Windows Installer e pode retornar um estado de recurso de INSTALLstate \_ BADCONFIG.

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Sinalizador de bits</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </dl> O componente não pode ser executado da origem. Defina esse bit para todos os componentes que pertencem a um recurso para impedir que o recurso seja executado da rede ou executado da fonte. Observe que, se um recurso não tiver componentes, o recurso sempre mostrará executar-de-origem e executar-de-meu-Computer como opções válidas.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </dl> O componente só pode ser executado da origem. Defina esse bit para todos os componentes que pertencem a um recurso para impedir que o recurso seja executado-de-meu computador. Observe que, se um recurso não tiver componentes, o recurso sempre mostrará executar-de-origem e executar-de-meu-Computer como opções válidas.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </dl> O componente pode ser executado localmente ou da origem.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </dl> Se esse bit for definido, o valor na coluna KeyPath será usado como uma chave na <a href="registry-table.md">tabela do registro</a>. Se o campo de valor do registro correspondente na tabela de registro for nulo, o campo de nome nesse registro não deverá conter &quot; + &quot; , &quot; - &quot; ou &quot; * &quot; . Para obter mais informações, consulte a descrição do campo nome na <a href="registry-table.md">tabela do registro</a>.<br/> Definir esse bit é recomendado para entradas do registro gravadas no hive HKCU. Isso garante que o instalador grave as entradas de Registro HKCU necessárias quando houver vários usuários no mesmo computador.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </dl> Se esse bit for definido, o instalador incrementará a contagem de referência no registro de DLL compartilhado do arquivo de chave do componente. Se esse bit não estiver definido, o instalador incrementará a contagem de referência somente se a contagem de referência já existir.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </dl> Se esse bit estiver definido, o instalador não removerá o componente durante uma desinstalação. O instalador registra um cliente de sistema extra para o componente no Windows Installer configurações do registro.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </dl> Se esse bit for definido, o valor na coluna KeyPath será uma chave para a <a href="odbcdatasource-table.md">tabela ODBCDataSource</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </dl> Se esse bit for definido, o instalador reavaliará o valor da instrução na coluna condição após uma reinstalação. Se o valor era falso anteriormente e foi alterado para true, o instalador instalará o componente. Se o valor era verdadeiro e foi alterado para false, o instalador removerá o componente, mesmo que o componente tenha outros produtos como clientes.<br/> Esse bit só deve ser definido para componentes transitivos. Consulte <a href="using-transitive-components.md">usando componentes transitivos</a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </dl> Se esse bit estiver definido, o instalador não instalará ou reinstalará o componente se um arquivo de caminho de chave ou uma entrada de registro de caminho de chave para o componente já existir. O aplicativo se registra como um cliente do componente.<br/> Use este sinalizador somente para componentes que estão sendo registrados pela tabela do registro. Não use esse sinalizador para os componentes registrados pelas tabelas <a href="appid-table.md">AppID</a>, <a href="class-table.md">classe</a>, <a href="extension-table.md">extensão</a>, <a href="progid-table.md">ProgID</a>, <a href="mime-table.md">MIME</a>e <a href="verb-table.md">verbo</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </dl> Defina esse bit para marcá-lo como um componente de 64 bits. Esse atributo facilita a instalação de pacotes que incluem componentes de 32 bits e 64 bits. Se esse bit não estiver definido, o componente será registrado como um componente de 32 bits.<br/> Se este for um componente de 64 bits substituindo um componente de 32 bits, defina esse bit e atribua um novo GUID na coluna ComponentID.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </dl> Defina esse bit para desabilitar a <a href="/windows/desktop/WinProg64/registry-reflection">reflexão do registro</a> em todas as chaves de registro existentes e novas afetadas por esse componente. Se esse bit for definido, o Windows Installer chamará o <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> em cada chave que estiver sendo acessada pelo componente. Esse bit está disponível com Windows Installer versão 4,0. Esse bit é ignorado em sistemas de 32 bits. Esse bit é ignorado nas versões de 64 bits do Windows XP.<br/>
<blockquote>
[!Note]<br />
os aplicativos do Windows de 32 bits em execução no emulador do Windows de 64 bits (WOW64) referem-se a uma exibição diferente do registro do que os aplicativos de 64 bits. A reflexão do registro copia alguns valores do registro entre essas duas exibições do registro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </dl> Defina esse bit para um componente em um pacote de patch para evitar a saída de componentes órfãos no computador. Se um patch subsequente estiver instalado, marcado com o valor <strong>msidbPatchSequenceSupersedeEarlier</strong> em sua tabela <a href="msipatchsequence-table.md">MsiPatchSequence</a> para substituir o primeiro patch, Windows Installer 4,5 e posterior poderá cancelar o registro e desinstalar os componentes marcados com o valor <strong>msidbComponentAttributesUninstallOnSupersedence</strong> . Se o componente não estiver marcado com esse bit, a instalação de um patch substituto poderá deixar por trás de um componente não utilizado no computador.<br/> Definir a propriedade <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> tem o mesmo efeito que definir esse bit para todos os componentes.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 e anterior</a>:</strong> não há suporte para o valor <strong>msidbComponentAttributesUninstallOnSupersedence</strong> e ele é ignorado.<br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </dl> Se um componente estiver marcado com esse valor de atributo em pelo menos um pacote instalado no sistema, o instalador tratará o componente como marcado em todos os pacotes. Se um pacote que compartilha o componente marcado for desinstalado, Windows Installer 4,5 poderá continuar a compartilhar a versão mais recente do componente no sistema, mesmo que a versão mais recente tenha sido instalada pelo pacote que está sendo desinstalado. <br/> Se a política DisableSharedComponent for definida como 1, nenhum pacote obterá a funcionalidade de componente compartilhado habilitada por este bit.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 e anterior</a>:</strong> não há suporte para o valor <strong>msidbComponentAttributesShared</strong> e ele é ignorado.<br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Esta coluna contém uma instrução condicional que pode controlar se um componente está instalado. Se a condição for nula ou for avaliada como true, o componente será habilitado. Se a condição for avaliada como false, o componente será desabilitado e não será instalado.

O campo condição habilita ou desabilita um componente somente durante a [ação CostFinalize](costfinalize-action.md). Para habilitar ou desabilitar um componente após o CostFinalize, você deve usar uma ação personalizada ou o [ControlEvent, DoAction](doaction-controlevent.md) para chamar [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea).

Observe que, a menos que o bit transitiva na coluna atributos esteja definido para um componente, o componente permanecerá habilitado uma vez instalado, mesmo se a instrução condicional na coluna condição for avaliada como false em uma instalação de manutenção subsequente do produto.

A coluna condição na tabela de componentes aceita expressões condicionais que contêm referências aos Estados instalados de recursos e componentes. Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath
</dt> <dd>

Esse valor aponta para um arquivo ou pasta que pertence ao componente que o instalador usa para detectar o componente. Dois componentes não podem compartilhar o mesmo valor de caminho de chave. O valor nessa coluna também é o caminho retornado pela função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .

Se o valor não for nulo, o KeyPath será uma chave primária para as tabelas [Registry](registry-table.md), [ODBCDataSource](odbcdatasource-table.md)ou [File](file-table.md) , dependendo do valor do atributo. Se KeyPath for NULL, a pasta da \_ coluna Directory será usada como o caminho da chave.

Como as pastas criadas pelo instalador são excluídas quando se tornam vazias, você deve criar uma entrada na [tabela CreateFolder](createfolder-table.md) para instalar um componente que consiste em uma pasta vazia.

Observe que, se um componente de Windows Installer contiver um arquivo ou chave do Registro protegido por [proteção de recursos do Windows](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) ou um arquivo protegido pela WFP (proteção de arquivo do Windows), esse recurso deverá ser usado como o caminho de chave para o componente. Nesse caso, Windows Installer não instala, atualiza ou remove o componente. Você não deve incluir nenhum recurso protegido em um pacote de instalação. Em vez disso, você deve usar os [mecanismos de substituição de recursos com suporte](/windows/desktop/Wfp/supported-file-replacement-mechanisms) para proteção de recursos do Windows. Para obter mais informações, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter uma discussão sobre a relação entre componentes e recursos, consulte [tabela de recursos](feature-table.md).

O instalador controla as DLLs compartilhadas independentemente da contagem de referência de DLL compartilhada no registro. Se houver uma contagem de referência para uma DLL compartilhada no registro, o instalador sempre incrementará a contagem quando estiver instalando o arquivo e o decrementará quando estiver desinstalando. Se **msidbComponentAttributesSharedDllRefCount**, não estiver definido, e a contagem de referência ainda não existir, o instalador não criará um. Observe que a contagem de referência de SharedDLLs no registro é incrementada para todos os arquivos instalados na pasta do sistema.

Se **msidbComponentAttributesSharedDllRefCount** não for definido, outro aplicativo poderá remover o componente, mesmo que ainda seja necessário. Para ver como isso pode acontecer, considere o seguinte cenário:

-   Um aplicativo que usa o instalador instala um componente compartilhado.
-   O bit **msidbComponentAttributesSharedDllRefCount** não está definido e não há nenhuma contagem de referência. Portanto, o instalador não inicia uma contagem de referência.
-   Um aplicativo herdado que compartilha esse componente e não usa o instalador está instalado.
-   O aplicativo herdado cria e incrementa uma contagem de referência para o componente compartilhado.
-   O aplicativo herdado é desinstalado.
-   A contagem de referência para o componente compartilhado é diminuída para zero e o componente é removido.
-   O aplicativo que usa o instalador não tem mais acesso ao componente.

Para evitar esse comportamento, defina **msidbComponentAttributesSharedDllRefCount**.

Observe que os componentes dos serviços do sistema não devem ser especificados como execução de origem sem serem projetados especificamente para tal uso. Consulte a [tabela de instalação](serviceinstall-table.md) para obter mais detalhes.

Observe que os atributos que habilitam a instalação de execução da origem nunca devem ser definidos para componentes que contêm bibliotecas de vínculo dinâmico que vão para a pasta do sistema. O motivo é que, se o estado da instalação do componente se tornar definido como execução da fonte seguindo um recurso ou definido na interface do usuário, as chamadas subsequentes para **LoadLibrary** na DLL falharão.

Consulte também, [controlando os Estados de seleção de recursos](controlling-feature-selection-states.md).

## <a name="validation"></a>Validação

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

