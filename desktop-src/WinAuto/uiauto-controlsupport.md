---
title: Suporte de automação de interface do usuário para Controles Padrão
description: Este tópico identifica os controles padrão do Windows com suporte pela automação da interface do usuário da Microsoft. O suporte completo é fornecido apenas para controles da versão 6 do ComCtrl32.dll (disponível com o Windows XP e posterior).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- clientes, suporte de automação da interface do usuário para controles padrão
- clientes, suporte a controle padrão
- clientes, controles do Win32
- Automação da interface do usuário, suporte para controles padrão
- Automação da interface do usuário, suporte a controle padrão
- Automação da interface do usuário, controles do Win32
- suporte para controles padrão
- suporte de controle padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498626"
---
# <a name="ui-automation-support-for-standard-controls"></a>Suporte de automação de interface do usuário para Controles Padrão

Este tópico identifica os controles padrão do Windows com suporte pela automação da interface do usuário da Microsoft. O suporte completo é fornecido apenas para controles da versão 6 do ComCtrl32.dll (disponível com o Windows XP e posterior).

> [!Note]  
> O controle RichEdit tem suporte apenas para versões fornecidas com o Windows Vista (no RichEd20.dll versão 3,1 e posterior e MsftEdit.dll versão 4,1 e posterior).

 

A tabela a seguir lista os nomes de classe dos controles padrão com suporte, juntamente com os tipos de controle de automação da interface do usuário correspondentes.



| Nome da Classe          | Tipo de controle        |
|---------------------|---------------------|
| Botão              | Botão              |
| Botão              | RadioButton         |
| Botão              | Agrupar               |
| Botão              | CheckBox            |
| Botão              | Hyperlink           |
| Botão              | SplitButton         |
| Botão              | CheckBox            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| Editar                | Documento            |
| Editar                | Editar                |
| SysLink             | Hyperlink           |
| Estático              | Texto                |
| Estático              | Imagem               |
| SysIPAddress32      | Personalizado              |
| SysHeader32         | Cabeçalho/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | Lista                |
| ListBox             | Lista                |
| ListBox             | Item            |
| \#32768             | Menu                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | ProgressBar         |
| RichEdit            | Documento. Veja a observação. |
| RichEdit20A         | Documento            |
| RichEdit20W         | Documento            |
| RichEdit50W         | Documento            |
| ScrollBar           | Controle deslizante              |
| msctls \_ trackbar32  | Controle deslizante              |
| msctls \_ updown32    | Controle giratório             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | Tab                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Botão              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Separador           |
| Dicas de ferramenta \_ class32   | ToolTip             |
| \#32774             | ToolTip             |
| ReBarWindow32       | Barra de ferramentas             |
| SysTreeView32       | Árvore                |
| SysTreeView32       | TreeItem            |



 

Não há suporte para os controles listados na tabela a seguir.



| Nome da Classe                                    | Tipo de controle |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | Imagem        |
| SysPager                                      | Controle giratório      |
| SysDateTimePick32                             | Personalizado       |
| SysMonthCal32                                 | Calendário     |
| MS \_ WINNOTE                                   | Dica de ferramenta      |
| VBBubble                                      | Dica de ferramenta      |
| ScrollBar (quando usado como um controle autônomo) | Controle deslizante       |
| Subgrade                                     | Personalizado       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




