---
description: Controles e texto colocados em caixas de diálogo e painéis permitem que o usuário interaja com o processo de instalação.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Adicionando controles e texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58602c4d793b25e1670373773ac8d3f5be2399c6351e56ebe2de1579c78ddcc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046026"
---
# <a name="adding-controls-and-text"></a>Adicionando controles e texto

Controles e texto colocados em caixas de diálogo e painéis permitem que o usuário interaja com o processo de instalação. Adicione uma caixa de diálogo à interface do usuário, incluindo-a na tabela [Diálogo,](dialog-table.md) conforme descrito em Usando o [Interface do Usuário](using-the-user-interface.md). Preencha caixas de diálogo e painéis com controles preenchendo a tabela [Control e](control-table.md) a [tabela BBControl,](bbcontrol-table.md)respectivamente.

Os atributos iniciais do controle podem ser especificados na coluna Atributos da [tabela Controle](control-table.md). Consulte [Atributos de controle](control-attributes.md).

Para tornar os atributos de controle dependentes de uma condição, use a tabela [ControlCondition](controlcondition-table.md) para desabilitar, habilitar, ocultar ou mostrar um controle de acordo com o valor de uma propriedade ou instrução condicional. Você também pode usar essa tabela para substituir a especificação do controle padrão inserido na [tabela Dialog](dialog-table.md).

Para que um evento altere um atributo de controle, assine o controle para um ControlEvent na [tabela EventMapping](eventmapping-table.md). Um ControlEvent especifica uma ação a ser tomada pelo instalador ou uma alteração nos atributos de um ou mais controles na caixa de diálogo. Consulte [Visão geral do ControlEvent.](controlevent-overview.md) Insira o identificador do atributo na coluna Atributo e o identificador do ControlEvent na coluna Evento da [tabela EventMapping](eventmapping-table.md).

Alguns controles facilitam a coleta de informações do usuário. Por exemplo, uma caixa de seleção permite ao usuário definir o valor de uma propriedade. Consulte a [tabela CheckBox](checkbox-table.md), a [tabela ComboBox](combobox-table.md), a tabela [ListBox](listbox-table.md), a [tabela RadioButton](radiobutton-table.md)e a [tabela ListView](listview-table.md).

Observe que, por motivos de segurança, as propriedades privadas não podem ser alteradas pelo usuário que interage com a interface do usuário. Se uma propriedade deve ser definida pela interface do usuário, ela precisa ser uma propriedade pública e ter um nome em todas as letras maiúsculas. Consulte [Sobre propriedades](about-properties.md).

Você pode fazer sua caixa de diálogo apresentar informações para o usuário ou gravar em um log em resposta às ações de instalação preenchendo a [tabela ActionText](actiontext-table.md).

Os controles podem ter um estilo de fonte predefinido. Para definir o estilo de fonte e fonte de uma cadeia de caracteres de texto, prefixe a cadeia de caracteres exibida com { style} ou \\ {&*style*}. Em que style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhum deles estiver presente, mas a [**propriedade DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.

É recomendável que a propriedade [**DefaultUIFont**](defaultuifont.md) de cada pacote [](property-table.md) de instalação com uma interface do usuário seja definida na tabela Propriedade para um dos estilos predefinidos listados na [tabela TextStyle](textstyle-table.md). Se essa propriedade não for especificada, o instalador usará a fonte System. Isso pode fazer com que o instalador exibe incorretamente cadeias de caracteres de texto se a página de código do pacote for diferente da página de código de interface do usuário padrão do usuário.

Para a maioria dos controles, o texto é exibido usando o conjunto de caracteres especificado pela página de código do banco de dados. Isso garante que o conjunto de caracteres correto seja usado com as informações contidas no banco de dados. As exceções a isso são os controles [Editar](edit-control.md), [DirectoryList](directorylist-control.md), [PathEdit](pathedit-control.md)e [DirectoryCombo,](directorycombo-control.md) que sempre exibem texto usando o conjunto de caracteres de interface do usuário padrão do usuário. Os [controles Text,](text-control.md) [ListBox](listbox-control.md)e [ComboBox](combobox-control.md) usarão o conjunto de caracteres de interface do usuário padrão do usuário se o Atributo de [Controle UsersLanguage](userslanguage-control-attribute.md) estiver definido.

Em alguns casos, um controle pode ser redesenhado incorretamente ao cancelar uma caixa de diálogo. Isso tem a ver com a ordem em que os controles recebem mensagens WM PAINT após a caixa de \_ diálogo Cancelar ser removida.  Para corrigir isso, tente alterar a ordem dos controles na tabela Controle.

Os controles devem ser grandes o suficiente para acomodar todo o texto exibido em todas as configurações de tamanho da fonte. Os controles devem ser grandes o suficiente para acomodar todo o texto localizado, se o texto na interface do usuário pode ser localizado. Tamanhos de fonte maiores ou texto localizado podem exigir mais espaço do que o texto original e podem ser truncados por um controle que se torna muito pequeno. Para obter mais informações sobre como localização de texto da interface do usuário, consulte a seção: [Um exemplo de localização](a-localization-example.md).

 

 



