---
description: A Tabela de Recursos define a estrutura de árvore lógica dos recursos e contém as colunas mostradas na tabela a seguir.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tabela de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dcf9177c44f407876cbe339925ca4524034a1335393161bb40310d60c158ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251756"
---
# <a name="feature-table"></a>Tabela de recursos

A Tabela de Recursos define a estrutura de árvore lógica dos recursos e contém as colunas mostradas na tabela a seguir.



| Coluna          | Tipo                         | Chave | Nullable |
|-----------------|------------------------------|-----|----------|
| Recurso         | [Identificador](identifier.md) | Y   | N        |
| Pai do \_ recurso | [Identificador](identifier.md) | N   | Y        |
| Título           | [Text](text.md)             | N   | Y        |
| Descrição     | [Text](text.md)             | N   | Y        |
| Exibir         | [Inteiro](integer.md)       | N   | Y        |
| Nível           | [Inteiro](integer.md)       | N   | N        |
| Diretório\_     | [Identificador](identifier.md) | N   | Y        |
| Atributos      | [Inteiro](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Recurso
</dt> <dd>

A chave primária usada para identificar um registro de recurso específico. O valor nesse campo não deve exceder um comprimento máximo de 38 caracteres.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Pai do \_ recurso
</dt> <dd>

Uma chave opcional de um registro pai na mesma tabela.

A chave aponta para a coluna Recurso. Se o recurso pai não estiver selecionado, esse recurso não será instalado. Um valor nulo nesse campo indica que esse recurso não tem um pai e é um item raiz. A coluna \_ Pai do Recurso não deve ser igual à coluna Recurso do mesmo registro.

> [!Note]  
> A profundidade máxima de qualquer recurso é 16. Um [erro 2701](windows-installer-error-messages.md) resulta se existir um recurso que excede essa profundidade máxima.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Uma cadeia de caracteres curta de texto que identifica um recurso.

Essa cadeia de caracteres é listada como um item pelo [Controle SelectionTree](selectiontree-control.md) da caixa [de diálogo Seleção](selection-dialog.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

Uma cadeia de caracteres mais longa de texto que descreve um recurso.

Essa cadeia de caracteres localizável é exibida pelo Controle [de Texto](text-control.md) da Caixa de Diálogo [de Seleção](selection-dialog.md).

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Exibir
</dt> <dd>

O número nesse campo especifica a ordem em que o recurso deve ser exibido na interface do usuário.

O valor também determina se o recurso é exibido inicialmente expandido ou recolhido. Se o valor for nulo ou 0 (zero), o registro não será exibido.

-   Se o valor for ímpar, o nó de recurso será expandido inicialmente.
-   Se o valor for even, o nó de recurso será recolhido inicialmente.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Nível
</dt> <dd>

O nível de instalação inicial desse recurso. O processamento da [Tabela de Condição](condition-table.md) pode modificar o valor de nível.

Um nível de instalação de 0 (zero) desabilita o item e impede que ele seja exibido. Um recurso com um nível de instalação de 0 (zero) não é instalado durante qualquer instalação, incluindo instalações administrativas. Para obter mais informações, consulte as informações de "Nível de Instalação" na seção Comentários deste tópico.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Diretório\_
</dt> <dd>

A coluna Diretório especifica o nome de um diretório que pode ser configurado por uma \_ Caixa de Diálogo de [Seleção](selection-dialog.md).

Como esse campo é uma chave na Tabela [de](directory-table.md)Diretórios , o diretório especificado deve ser listado na primeira coluna da Tabela de Diretórios. Você deve inserir uma [Propriedade Pública](public-properties.md) nessa coluna para tornar o diretório configurável e exibir um **botão** Procurar na Caixa de Diálogo [de Seleção](selection-dialog.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

A opção de execução remota para recursos que não estão instalados e para os quais nenhuma solicitação de estado de recurso é feita usando qualquer uma das propriedades a seguir.

-   [**Propriedade ADDLOCAL**](addlocal.md)
-   [**Propriedade ADDSOURCE**](addsource.md)
-   [**Propriedade ADDDEFAULT**](adddefault.md)
-   [**Propriedade COMPADDLOCAL**](compaddlocal.md)
-   [**Propriedade COMPADDSOURCE**](compaddsource.md)
-   [**Propriedade FILEADDLOCAL**](fileaddlocal.md)
-   [**Propriedade FILEADDSOURCE**](fileaddsource.md)
-   [**Propriedade REMOVE**](remove.md)
-   [**Propriedade REINSTALL**](reinstall.md)
-   [**Propriedade ADVERTISE**](advertise.md)

Adicione os bits indicados ao valor total dessa coluna para incluir uma opção de execução remota.

-   Se esse campo estiver em branco, o valor será padrão como 0 (zero), msidbFeatureAttributesFavorLocal.
-   Se o nível de instalação do recurso for 0 (zero) ou maior ou igual ao nível de instalação atual, nenhuma alteração será feita no estado do recurso.



| Nome                                         | Decimal | Hexadecimal | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | Os componentes desse recurso que não estão marcados para instalação da origem são instalados localmente. Um componente compartilhado por dois ou mais recursos, alguns dos quais são definidos como msidbFeatureAttributesFavorLocal e outros como msidbFeatureAttributesFavorSource, é instalado localmente. Componentes marcados como msidbComponentAttributesSourceOnly na Tabela de Componentes são sempre executados no CD/servidor de origem. [](component-table.md) Os bits msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funcionam com recursos não listados pela [**propriedade ADVERTISE**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | Os componentes desse recurso não marcados para instalação local são instalados para serem executados do CD-ROM ou do servidor de origem. Um componente compartilhado por dois ou mais recursos, alguns dos quais são definidos como msidbFeatureAttributesFavorLocal e outros para o msidbFeatureAttributesFavorSource, é instalado para ser executado localmente. Os componentes marcados como msidbComponentAttributesLocalOnly na [tabela de componentes](component-table.md) são sempre instalados localmente. Os bits msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funcionam com recursos não listados pela [**Propriedade advertise**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Defina esse atributo e o estado do recurso será o mesmo que o estado do pai do recurso. Você não poderá usar essa opção se o recurso estiver localizado na raiz de uma árvore de recursos. Omita esse atributo e o estado do recurso é determinado de acordo com msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Para garantir que o estado do recurso filho sempre siga o estado de seu pai, mesmo quando o filho e o pai estão inicialmente definidos como ausentes no controle SelectionTree, você deve incluir msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent nos atributos do recurso filho.<br/> Observe que se você definir msidbFeatureAttributesFollowParent sem definir msidbFeatureAttributesUIDisallowAbsent, o instalador não poderá forçar o recurso filho do estado ausente. Nesse caso, o recurso filho corresponde ao estado de instalação do pai somente se o filho estiver definido como algo diferente de ausente.<br/> Defina msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent para garantir que um recurso filho siga o estado do recurso pai.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Defina esse atributo e o estado do recurso será Advertise. Se o recurso for listado pela [**Propriedade ADDDEFAULT**](adddefault.md) , esse bit será ignorado e o estado do recurso será determinado de acordo com MsidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource. Omita esse atributo e o estado do recurso é determinado de acordo com msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Observe que esse bit funciona apenas com os recursos listados pela [**Propriedade advertise**](advertise.md). Defina esse atributo para impedir que o recurso seja anunciado.<br/> Defina esse atributo e, se o recurso listado não for pai ou filho, o recurso será instalado de acordo com msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Defina esse atributo para o pai de um recurso listado e o pai será instalado.<br/> Defina este atributo para o filho de um recurso listado e o estado do filho está ausente.<br/> Omita esse atributo e, se o recurso listado não for pai ou filho, o estado do recurso será Advertise.<br/> Omita esse atributo e, se o recurso listado for pai ou filho, o estado de ambos os recursos será Advertise.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Defina esse atributo e a interface do usuário não exibirá uma opção para alterar o estado do recurso para ausente. A configuração desse atributo força o recurso para o estado de instalação, independentemente de o recurso estar visível na interface do usuário ou não. Omita esse atributo e a interface do usuário exibe uma opção para alterar o estado do recurso para ausente.<br/> Defina msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent para garantir que um recurso filho siga o estado do recurso pai.<br/> Definir esse atributo não afeta apenas a interface do usuário, mas também força o recurso para o estado de instalação, independentemente de o recurso estar visível na interface do usuário ou não.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | defina este atributo e o anúncio será desabilitado para o recurso se o shell do sistema operacional não oferecer suporte a descritores de Windows Installer. Omita este atributo e o anúncio não está desabilitado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Alguns atributos são exclusivos um do outro. A tentativa de definir esses atributos juntos no mesmo recurso faz com que o pacote de instalação falhe na [**validação do pacote**](package-validation.md).

-   Não use msidbFeatureAttributesFavorAdvertise com msidbFeatureAttributesDisallowAdvertise.
-   Não use msidbFeatureAttributesNoUnsupportedAdvertise com msidbFeatureAttributesDisallowAdvertise juntos.
-   Não use msidbFeatureAttributesFollowParent com msidbFeatureAttributesFavorSource.
-   Observe que os valores msidbFeatureAttributesFollowParent e msidbFeatureAttributesFavorLocal são mutuamente exclusivos. Se o valor de msidbFeatureAttributesFollowParent for usado, o valor de msidbFeatureAttributesFavorLocal será considerado como inexistente.

</dd> </dl>

Observe que, se um recurso filho estiver instalado, seu recurso pai também será instalado. Se um recurso pai estiver instalado, seu recurso filho não será necessariamente instalado, a menos que seus atributos msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent sejam definidos. Essa relação hierárquica da instalação de recursos pai e filho também é usada para instalações de GUI e instalações que usam Propriedades de linha de comando.

## <a name="remarks"></a>Comentários

Várias colunas temporárias adicionais são adicionadas a essa tabela quando ela é carregada na memória para computações usadas pela seleção de custos e de interface do usuário.

Um componente pode ser compartilhado entre dois ou mais recursos ou aplicativos. Se dois ou mais recursos fizerem referência ao mesmo componente, esse componente será selecionado para instalação se qualquer um dos recursos associados for selecionado. Isso também pode ser o motivo pelo qual os recursos filho não são desinstalados quando um recurso pai é removido. se o recurso filho consistir em componentes necessários para outros recursos ou aplicativos, o Windows Installer não removerá o recurso filho.

Para obter mais informações, consulte [controlando Estados de seleção de recursos](controlling-feature-selection-states.md).

Nível de instalação:

-   Para qualquer instalação, há um nível de instalação definido, que é um valor integral de 1 a 32.767. O valor inicial é determinado pela [**Propriedade INSTALLLEVEL**](installlevel.md), que é definida na tabela de [Propriedades](property-table.md).
-   Um recurso será instalado somente se o valor de nível de recurso for menor ou igual ao nível de instalação atual. A interface do usuário pode ser criada para que, quando a instalação for inicializada, o instalador permita que o usuário modifique o nível de instalação de qualquer recurso na tabela de recursos. Por exemplo, um autor pode definir valores de nível de instalação que representam opções de instalação específicas, como **personalizada**, **típica** ou **mínima**, e, em seguida, criar uma caixa de diálogo que usa [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) para permitir que o usuário selecione um desses Estados.
-   Dependendo do estado que o usuário seleciona, a caixa de diálogo define a propriedade nível de instalação como o valor correspondente. Se o autor atribuir um nível **típico** de 100 e o usuário selecionar **típica**, somente os recursos com um nível de 100 ou menos serão instalados. Além disso, a opção **personalizada** pode levar a outra caixa de diálogo que contém um [controle SelectionTree](selectiontree-control.md). O controle SelectionTree permite que o usuário altere individualmente se cada recurso está instalado ou não.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




