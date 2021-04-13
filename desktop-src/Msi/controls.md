---
description: Os desenvolvedores de pacotes de instalação podem criar uma interface do usuário que contém os controles discutidos neste tópico.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: Controles (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec286adf25c0642ae044bfd0b89e66182ef6839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297698"
---
# <a name="controls-windows-installer"></a>Controles (Windows Installer)

Os desenvolvedores de pacotes de instalação podem criar uma interface do usuário que contém os controles discutidos neste tópico. Para obter informações sobre como adicionar um controle específico a uma caixa de diálogo, consulte o tópico desse controle e leia a seção [adicionando controles e texto](adding-controls-and-text.md).

Alguns controles, como CheckBox e ComboBox, são associados a uma propriedade especificada na coluna Property da [tabela de controle](control-table.md). Um usuário altera o valor dessa propriedade interagindo com o controle. Os controles passivos, como o mural e o bitmap, não estão associados a tal propriedade.

Por segurança, as propriedades privadas não podem ser alteradas por um usuário interagindo com a interface do usuário. Para que uma propriedade seja definida pela interface do usuário, ela precisa ser uma propriedade pública e em letras maiúsculas. Consulte também [sobre propriedades](about-properties.md).

Em alguns casos, um controle pode ser redesenhado incorretamente ao cancelar uma caixa de diálogo. Isso tem a ver com a ordem em que os controles recebem mensagens do WM \_ Paint depois que a caixa de diálogo de cancelamento é removida. Para corrigir isso, tente alterar a ordem dos controles na tabela de controle.



| Nome do controle                                       | Propriedade associada | Breve descrição do controle                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mensagem](billboard-control.md)                 | No                  | Exibe os murals com base nas mensagens de progresso.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | No                  | Exibe uma imagem estática de um bitmap.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Yes                 | Uma caixa de seleção de dois Estados.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Yes                 | Uma lista suspensa com um campo de edição.                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Yes                 | Selecione tudo, exceto o último segmento do caminho.                                                                                                                                       |
| [Directorylist](directorylist-control.md)         | Yes                 | Exibe as pastas abaixo da parte principal do caminho.                                                                                                                                         |
| [Editar](edit-control.md)                           | Yes                 | Um campo de edição regular para qualquer cadeia de caracteres ou inteiro.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | No                  | Exibe um retângulo que agrupa outros controles juntos.                                                                                                                             |
| [Hiperlink](hyperlink-control.md)                 | No                  | Exibe um link HTML para um endereço, que é aberto no navegador padrão. **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/> |
| [Ícone](icon-control.md)                           | No                  | Exibe uma imagem estática de um ícone.                                                                                                                                                 |
| [Linha](line-control.md)                           | No                  | Exibe uma linha horizontal.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Yes                 | Uma lista suspensa sem um campo de edição.                                                                                                                                               |
| [ListView](listview-control.md)                   | Yes                 | Exibe uma coluna de valores com ícones para seleção.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Yes                 | Um campo de edição com uma máscara no campo de texto.                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Yes                 | Exibe o nome da pasta ou o caminho inteiro em um campo de edição.                                                                                                                                 |
| [Controle ProgressBar](progressbar-control.md)     | No                  | Gráfico de barras que muda de comprimento enquanto recebe mensagens de progresso.                                                                                                                       |
| [Botão](pushbutton-control.md)               | No                  | Exibe um botão de ação básico.                                                                                                                                                         |
| [Botão de opção](radiobuttongroup-control.md)   | Yes                 | Um grupo de botões de opção.                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | No                  | Exibe uma cadeia de caracteres longa de texto.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Yes                 | Exibe informações da tabela de recursos e permite que o usuário altere seu estado de seleção.                                                                                     |
| [Text](text-control.md)                           | No                  | Exibe texto estático.                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | No                  | Exibe informações de custo em volumes diferentes.                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Yes                 | Seleciona o volume de uma lista alfabética.                                                                                                                                             |



 

 

 




