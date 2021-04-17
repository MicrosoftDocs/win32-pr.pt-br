---
description: Os controles e o texto colocados nas caixas de diálogo e nos murals permitem que o usuário interaja com o processo de instalação.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Adicionando controles e texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749597"
---
# <a name="adding-controls-and-text"></a>Adicionando controles e texto

Os controles e o texto colocados nas caixas de diálogo e nos murals permitem que o usuário interaja com o processo de instalação. Adicione uma caixa de diálogo à interface do usuário, incluindo-a na [tabela de diálogo](dialog-table.md) , conforme descrito em [usando a interface do usuário](using-the-user-interface.md). Preencha caixas de diálogo e murals com controles populando a [tabela de controle](control-table.md) e a [tabela BBControl](bbcontrol-table.md), respectivamente.

Os atributos iniciais do controle podem ser especificados na coluna atributos da tabela de [controle](control-table.md). Consulte [atributos de controle](control-attributes.md).

Para tornar os atributos de controle dependentes de uma condição, use a [tabela ControlCondition](controlcondition-table.md) para desabilitar, habilitar, ocultar ou mostrar um controle de acordo com o valor de uma propriedade ou instrução condicional. Você também pode usar essa tabela para substituir a especificação do controle padrão inserido na tabela de [diálogo](dialog-table.md).

Para que um evento altere um atributo de controle, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md). Um ControlEvent, especifica uma ação a ser tomada pelo instalador ou uma alteração nos atributos de um ou mais controles na caixa de diálogo. Consulte [visão geral do ControlEvent,](controlevent-overview.md). Insira o identificador do atributo na coluna de atributo e o identificador do ControlEvent, na coluna evento da [tabela EventMappings](eventmapping-table.md).

Alguns controles facilitam a coleta de informações do usuário. Por exemplo, uma caixa de seleção permite que o usuário defina o valor de uma propriedade. Consulte a tabela de [caixas de seleção](checkbox-table.md), a [tabela ComboBox](combobox-table.md), a [tabela ListBox](listbox-table.md), a tabela [RadioButton](radiobutton-table.md)e a [tabela ListView](listview-table.md).

Observe que, por motivos de segurança, as propriedades privadas não podem ser alteradas pelo usuário interagindo com a interface do usuário. Se uma propriedade for ser definida pela interface do usuário, ela precisará ser uma propriedade pública e ter um nome em todas as letras maiúsculas. Consulte [sobre propriedades](about-properties.md).

Você pode fazer com que sua caixa de diálogo apresente informações ao usuário ou gravá-las em um log em resposta a ações de instalação preenchendo a [tabela ActionText](actiontext-table.md).

Os controles podem ter um estilo de fonte predefinido. Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&*Style*}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.

É recomendável que a propriedade [**DefaultUIFont**](defaultuifont.md) de cada pacote de instalação com uma interface do usuário seja definida na [tabela de propriedades](property-table.md) para um dos estilos predefinidos listados na [tabela TextStyle](textstyle-table.md). Se essa propriedade não for especificada, o instalador usará a fonte do sistema. Isso pode fazer com que o instalador exiba incorretamente cadeias de caracteres de texto se a página de código do pacote for diferente da página de código padrão da interface do usuário.

Para a maioria dos controles, o texto é exibido usando o conjunto de caracteres especificado pela página de código do banco de dados. Isso garante que o conjunto de caracteres correto seja usado com as informações contidas no banco de dados. As exceções a isso são os controles [Edit](edit-control.md), [directorylist](directorylist-control.md), [PathEdit](pathedit-control.md)e [DirectoryCombo](directorycombo-control.md) , que sempre exibem texto usando o conjunto de caracteres padrão da interface do usuário. Os controles de [texto](text-control.md), caixa de [listagem](listbox-control.md)e caixa de [combinação](combobox-control.md) usam o conjunto de caracteres padrão da interface do usuário, se o [atributo de controle UsersLanguage](userslanguage-control-attribute.md) estiver definido.

Em alguns casos, um controle pode ser redesenhado incorretamente ao cancelar uma caixa de diálogo. Isso tem a ver com a ordem em que os controles recebem mensagens do WM \_ Paint depois que a caixa de diálogo **Cancelar** é removida. Para corrigir isso, tente alterar a ordem dos controles na tabela de controle.

Os controles devem ser grandes o suficiente para acomodar todo o texto exibido em todas as configurações de tamanho de fonte. Os controles devem ser grandes o suficiente para acomodar todo o texto localizado, se o texto na interface do usuário puder ser localizado. Tamanhos de fonte maiores ou texto localizado podem exigir mais espaço do que o texto original e podem ser truncados por um controle que é muito pequeno. Para obter mais informações sobre como localizar o texto da interface do usuário, consulte a seção: [um exemplo de localização](a-localization-example.md).

 

 



