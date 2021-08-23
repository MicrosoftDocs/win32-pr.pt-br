---
description: A tabela de diálogo contém todas as caixas de diálogo que aparecem na interface do usuário (IU) nos modos completo e reduzido.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Tabela de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554bc551b41a7ebeaa8b63b2a0d1b74a0f55cfb1d7a087936a394a060286caba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692836"
---
# <a name="dialog-table"></a>Tabela de diálogo

A tabela de diálogo contém todas as caixas de diálogo que aparecem na interface do usuário (IU) nos modos completo e reduzido.

A tabela de diálogo tem as colunas a seguir.



| Coluna           | Tipo                               | Chave | Nullable |
|------------------|------------------------------------|-----|----------|
| caixa de diálogo           | [Identificador](identifier.md)       | Y   | N        |
| HCentering       | [Inteiro](integer.md)             | N   | N        |
| VCentering       | [Inteiro](integer.md)             | N   | N        |
| Largura            | [Inteiro](integer.md)             | N   | N        |
| Altura           | [Inteiro](integer.md)             | N   | N        |
| Atributos       | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Título            | [Binário](formatted.md)         | N   | Y        |
| Controlar \_ primeiro   | [Identificador](identifier.md)       | N   | N        |
| Padrão de controle \_ | [Identificador](identifier.md)       | N   | Y        |
| \_Cancelar controle  | [Identificador](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>'
</dt> <dd>

A chave primária e o nome da caixa de diálogo.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

A posição horizontal da caixa de diálogo.

O intervalo é de 0 a 100, com 0 na borda esquerda da tela e 100 na borda direita.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

A posição vertical da caixa de diálogo.

O intervalo é de 0 a 100, com 0 na borda superior da tela e 100 na borda inferior.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largura
</dt> <dd>

A largura do limite retangular da caixa de diálogo.

Esse número deve ser não negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Tamanho
</dt> <dd>

A altura do limite retangular da caixa de diálogo.

Esse número deve ser não negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Uma palavra de 32 bits que especifica os sinalizadores de atributo a serem aplicados a essa caixa de diálogo.

Esse número deve ser não negativo. Para obter mais informações, consulte o [estilo de caixa de diálogo bits](dialog-style-bits.md).

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Uma cadeia de caracteres de texto localizável que especifica o título a ser exibido na barra de título da caixa de diálogo.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Controlar \_ primeiro
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).

A combinação deste campo com o campo de caixa de diálogo especifica um controle exclusivo na [tabela de controle](control-table.md) que assume o foco quando a caixa de diálogo é aberta. Normalmente, isso pode ser um [controle de edição](edit-control.md), [controle SelectionTree](selectiontree-control.md)ou qualquer outro controle que possa assumir o foco. Se o [controle de pressão](pushbutton-control.md) for o único controle presente na caixa de diálogo que pode assumir o foco, o botão de pressão inserido no campo ControlDefault também deverá ser inserido no primeiro campo Control. Esta coluna é ignorada em uma caixa de [diálogo de erro](error-dialog.md) .

Como o texto estático não pode assumir o foco, um [controle de texto](text-control.md) que descreve um [controle de edição](edit-control.md), [controle PathEdit](pathedit-control.md), [controle ListView](listview-control.md), [controle ComboBox](combobox-control.md) ou [controle VolumeSelectCombo](volumeselectcombo-control.md) deve ser tornado o primeiro controle na caixa de diálogo para garantir a compatibilidade com leitores de tela.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Padrão de controle \_
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).

A combinação deste campo com o campo de caixa de diálogo especifica o controle padrão que entra em foco quando a caixa de diálogo é aberta. Normalmente, isso pode ser um [controle de pressão](pushbutton-control.md). Se nenhum controle de pressão na caixa de diálogo tiver o foco, a chave de retorno será equivalente a clicar no controle padrão. Se essa coluna for deixada em branco, não haverá nenhum controle padrão. Esta coluna é ignorada em uma caixa de [diálogo de erro](error-dialog.md) .

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>\_Cancelar controle
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).

A combinação deste campo com o campo de caixa de diálogo especifica um controle que cancela a instalação. Esse controle é acoplado a eventos na [tabela ControlEvent,](controlevent-table.md) usada para cancelar a instalação. Pressionar a tecla ESC ou clicar no botão fechar é equivalente a clicar no controle cancelar. Esta coluna é ignorada em uma [caixa de diálogo de erro](error-dialog.md)

quadro.

O controle de cancelamento é ocultado durante a reversão ou a remoção de arquivos de backup. O manipulador de interface do usuário interno oculta o controle ao receber uma \_ mensagem INSTALLMESSAGE COMMONDATA.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores inteiros para largura e altura estão nas [unidades do instalador](installer-units.md), não nas unidades de caixa de diálogo.

Os dois valores de centralização são ignorados para caixas de diálogo subsequentes em uma sequência de assistente. As posições da caixa de diálogo são definidas pelo usuário ou como para a caixa de diálogo anterior. Essas sequências de caixas de diálogo são criadas por um [NewDialog ControlEvent,](newdialog-controlevent.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



