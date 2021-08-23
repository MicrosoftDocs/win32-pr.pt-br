---
description: A tabela Atalho contém as informações que o aplicativo precisa para criar atalhos no computador do usuário.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabela de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628416"
---
# <a name="shortcut-table"></a>Tabela de atalho

A tabela Atalho contém as informações que o aplicativo precisa para criar atalhos no computador do usuário.

A tabela Atalho tem as seguintes colunas.



| Coluna                 | Tipo                         | Chave | Nullable |
|------------------------|------------------------------|-----|----------|
| Atalho               | [Identificador](identifier.md) | Y   | N        |
| Diretório\_            | [Identificador](identifier.md) | N   | N        |
| Nome                   | [Filename](filename.md)     | N   | N        |
| Componente\_            | [Identificador](identifier.md) | N   | N        |
| Destino                 | [Atalho](shortcut.md)     | N   | N        |
| Argumentos              | [Formatado](formatted.md)   | N   | Y        |
| Descrição            | [Text](text.md)             | N   | Y        |
| Tecla de acesso                 | [Inteiro](integer.md)       | N   | Y        |
| Ícone\_                 | [Identificador](identifier.md) | N   | Y        |
| IconIndex              | [Inteiro](integer.md)       | N   | Y        |
| ShowCmd                | [Inteiro](integer.md)       | N   | Y        |
| WkDir                  | [Identificador](identifier.md) | N   | Y        |
| DisplayResourceDLL     | [Formatado](formatted.md)   | N   | Y        |
| DisplayResourceId      | [Inteiro](integer.md)       | N   | Y        |
| DescriptionResourceDLL | [Formatado](formatted.md)   | N   | Y        |
| DescriptionResourceId  | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Atalho
</dt> <dd>

O valor da chave para esta tabela.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Diretório\_
</dt> <dd>

A chave externa na primeira coluna da [tabela Directory](directory-table.md). Essa coluna especifica o diretório no qual o arquivo De atalho é criado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

O nome localizável do atalho a ser criado.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

A chave externa na primeira coluna da [tabela Componente](component-table.md). O instalador usa o estado de instalação do componente especificado nesta coluna para determinar se o atalho é criado ou excluído. Esse componente deve ter um caminho de chave válido para o atalho a ser instalado. Se a coluna Destino contiver o nome de um recurso, o arquivo lançado pelo atalho será o arquivo de chave do componente listado nesta coluna.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

O destino de atalho.

Para um atalho anunciado, essa coluna deve ser uma chave externa na primeira coluna da [tabela Recurso](feature-table.md). O instalador avalia a entrada no campo Destino como um [Identificador](identifier.md) e a entrada deve ser uma chave estrangeira válida na Tabela [de Recursos](feature-table.md). O arquivo lançado pelo atalho nesse caso é o arquivo de chave do componente listado na coluna \_ Componente. Quando o atalho é ativado, o instalador verifica se todos os componentes no recurso estão instalados antes de iniciar esse arquivo.

Para um atalho não anunciado, o instalador avalia esse campo como uma [cadeia de caracteres formatada.](formatted.md) O campo deve conter um identificador de propriedade entre colchetes ( ), que é expandido para o arquivo ou uma pasta apontada \[ \] pelo atalho. Para obter mais informações, consulte [a ação CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Os argumentos de linha de comando para o atalho.

Observe que a resolução de propriedades no campo Argumentos é limitada. Uma propriedade formatada como Propriedade nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente que possui o \[  \] atalho estiver instalado. Por exemplo, para resolver para o valor correto para o argumento "MyDoc.doc", o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui o \[ \# \] atalho.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

A descrição localizável do atalho.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Tecla
</dt> <dd>

A tecla de atalhos do atalho. O byte de ordem inferior contém o código de chave virtual para a chave e o byte de ordem superior contém sinalizadores de modificador. Este deve ser um número não negativo. Os autores de pacotes de instalação geralmente são recomendados para não definir essa opção, pois a configuração dessa opção pode adicionar teclas de a-opções duplicadas à área de trabalho de um usuário. Além disso, a prática de atribuir teclas de atalho a atalhos pode ser problemática para os usuários que usam teclas de [acesso para acessibilidade](accessibility.md).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_
</dt> <dd>

A chave externa para a coluna um da [tabela de ícones](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

O índice de ícone do atalho. Este deve ser um número não negativo.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

O comando show para a janela do aplicativo.

Os valores a seguir podem ser usados. os valores são conforme definido para a Windows função de API de janela.



| Valor | Significado             |
|-------|---------------------|
| 1     | SW \_ normal      |
| 3     | SW não \_ maximizado   |
| 7     | \_SHOWMINNOACTIVE SW |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

O nome da propriedade que tem o caminho do diretório de trabalho para o atalho. o valor pode usar o formato Windows para referenciar variáveis de ambiente, por exemplo% USERPROFILE%. As referências são resolvidas para um caminho real quando o instalador resolve o diretório de trabalho para criar o atalho.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Esse campo contém um valor de cadeia de caracteres [formatado](formatted.md) para o caminho completo para o executável portátil neutro de idioma (arquivo ln) que contém os dados de configuração de recurso (RC config). A cadeia de caracteres formatada pode usar a \[ \# \] Convenção FileKey. Se esse campo contiver um valor, a coluna nome será ignorada. Se esse campo estiver vazio, o instalador usará o valor na coluna nome. Quando esse campo contiver um valor, o campo **DisplayResourceId** também será necessário para conter um valor ou a instalação falhará.

esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada. esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.

Para obter informações sobre como adicionar atalhos à tabela de atalho para uso com recursos de MUI, consulte [um exemplo de atalho do MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

O índice do nome de exibição do atalho. Este deve ser um número não negativo. Quando esse campo contém um valor, o campo **DisplayResourceDLL** também deve conter um valor ou a instalação falha.

esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada. esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Esse campo contém um valor de cadeia de caracteres [formatado](formatted.md) para o caminho completo para o executável portátil neutro de idioma (arquivo ln) que contém os dados de configuração de recurso (RC config). A cadeia de caracteres formatada pode usar a \[ \# \] Convenção FileKey. Se esse campo contiver um valor, a coluna nome será ignorada. Se esse campo estiver vazio, o instalador usará o valor na coluna Descrição. Quando esse campo contiver um valor, o campo **DescriptionResourceId** também será necessário para conter um valor ou a instalação falhará.

esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada. esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.

Para obter informações sobre como adicionar atalhos à tabela de atalho para uso com recursos de MUI, consulte [um exemplo de atalho do MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

O índice de nome de descrição do atalho. Este deve ser um número não negativo. Quando esse campo contém um valor, o campo **DescriptionResourceDLL** também deve conter um valor ou a instalação falha.

esta coluna da tabela de atalho é usada somente quando executada no Windows Vista ou no Windows Server 2008 e, caso contrário, é ignorada. esta coluna está disponível com versões não anteriores ao Windows Installer 4,0.

</dd> </dl>

## <a name="remarks"></a>Comentários

A habilitação de um recurso criará um atalho anunciado somente se a interface IShellLink do sistema der suporte à resolução do descritor de instalador. isso é suportado pelo microsoft Windows 2000 e sistemas que executam o microsoft Internet Explorer 4, 1. Se não houver suporte, o instalador criará um atalho não anunciado na instalação do componente do recurso, seja localmente ou executado a partir da origem.

Observe que os atalhos anunciados sempre apontam para um aplicativo específico, identificados por um [**ProductCode**](productcode.md)e não devem ser compartilhados entre aplicativos. Os atalhos anunciados só funcionam para o aplicativo instalado mais recentemente e são removidos quando esse aplicativo é removido.

Essa tabela é referida quando a [ação Createshortcuts](createshortcuts-action.md) e a [ação RemoveShortcuts](removeshortcuts-action.md) são executadas.

Consulte também a propriedade [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



