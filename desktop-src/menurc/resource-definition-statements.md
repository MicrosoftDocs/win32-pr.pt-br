---
title: Instruções Resource-Definition dados
description: As instruções de definição de recurso definem os recursos que o compilador de recursos coloca no recurso (. Res) file.
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilador de recursos, instruções de definição de recurso
- Recurso TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4937eb9d5fb9bba7b174aa9543be8b3f2eb41c90c6bc20a72650114f57fb4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869902"
---
# <a name="resource-definition-statements"></a>Instruções Resource-Definition dados

As instruções de definição de recurso definem os recursos que o compilador de recursos coloca no recurso (. Res) file. Após o . O arquivo Res está vinculado ao arquivo executável, o aplicativo pode carregar seus recursos em tempo de execução, conforme necessário. Todas as instruções de recurso associam um nome ou número de identificação a um determinado recurso.

As instruções de definição de recurso podem ser divididas nas seguintes categorias:

-   Recursos
-   Controles
-   Instruções

As tabelas a seguir descrevem as instruções de definição de recurso.

## <a name="resources"></a>Recursos



| Recurso                                      | Descrição                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aceleradores**](accelerators-resource.md) | Define as teclas de acelerador de menu.                                                                                                                                                  |
| [**Bitmap**](bitmap-resource.md)             | Define um bitmap nomeando-o e especificando o nome do arquivo que o contém. (Para usar um bitmap específico, o aplicativo o solicita por nome.)                          |
| [**Cursor**](cursor-resource.md)             | Define um cursor ou cursor animado nomeando-o e especificando o nome do arquivo que o contém. (Para usar um cursor específico, o aplicativo o solicita por nome.)       |
| [**Diálogo**](dialog-resource.md)             | Define um modelo que um aplicativo pode usar para criar caixas de diálogo.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Define um modelo que um aplicativo pode usar para criar caixas de diálogo.                                                                                                          |
| [**Fonte**](font-resource.md)                 | Especifica o nome de um arquivo que contém uma fonte.                                                                                                                              |
| [**HTML**](html-resource.md)                 | Especifica um arquivo HTML.                                                                                                                                                         |
| [**Ícone**](icon-resource.md)                 | Define um ícone ou ícone animado nomeando-o e especificando o nome do arquivo que o contém. (Para usar um ícone específico, o aplicativo o solicita por nome.)            |
| [**Menu**](menu-resource.md)                 | Define a aparência e a função de um menu.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Define a aparência e a função de um menu.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Define uma tabela de mensagens nomeando-a e especificando o nome do arquivo que a contém. O arquivo é um arquivo de recurso binário gerado pelo compilador de mensagem.                |
| [**Popup**](popup-resource.md)               | Define um item de menu que pode conter itens de menu e submenus.                                                                                                                   |
| **PLUGPLAY**                                  | Obsoleto.                                                                                                                                                                       |
| [**Rcdata**](rcdata-resource.md)             | Define recursos de dados. Os recursos de dados permitem incluir dados binários no arquivo executável.                                                                                      |
| [**Stringtable**](stringtable-resource.md)   | Define recursos de cadeia de caracteres. Os recursos de cadeia de caracteres são cadeias de caracteres Unicode ou ASCII que podem ser carregadas do arquivo executável.                                                            |
| **Textinclude**                               | Um recurso especial que é interpretado por Visual C++. Para obter mais informações, consulte [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Um recurso especial que é usado com as [opções de vinculador /TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) e [/TLBOUT.](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) |
| [**Definido pelo usuário**](user-defined-resource.md) | Define um recurso que contém dados específicos do aplicativo.                                                                                                                     |
| [**Versioninfo**](versioninfo-resource.md)   | Define um recurso de informações de versão. Contém informações como o número de versão, o sistema operacional pretendido e assim por diante.                                                  |
| **Vxd**                                       | Obsoleto.                                                                                                                                                                       |



 

Para obter mais informações sobre recursos MFC predefinidos, consulte [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) e [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Controles



| Control                                            | Descrição                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Cria um controle automático de caixa de seleção de três estados.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Cria um controle automático de caixa de seleção.                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | Cria um controle de botão de opção automático.                                  |
| [**Checkbox**](checkbox-control.md)               | Cria um controle de caixa de seleção.                                                |
| [**Combobox**](combobox-control.md)               | Cria um controle de caixa de combinação.                                                |
| [**Controle**](control-control.md)                 | Cria um controle definido pelo aplicativo.                                     |
| [**CTEXT**](ctext-control.md)                     | Cria um controle de texto centralizado.                                            |
| [**Defpushbutton**](defpushbutton-control.md)     | Cria um controle de pushbutton padrão.                                       |
| [**Edittext**](edittext-control.md)               | Cria um controle de edição.                                                    |
| [**Groupbox**](groupbox-control.md)               | Cria um controle de caixa de grupo.                                                |
| [**Ícone**](icon-control.md)                       | Cria um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo. |
| [**Listbox**](listbox-control.md)                 | Cria um controle de caixa de listagem.                                                 |
| [**Ltext**](ltext-control.md)                     | Cria um controle de texto alinhado à esquerda.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Cria um controle de caixa de push.                                                 |
| [**Botão**](pushbutton-control.md)           | Cria um controle de botão de push.                                              |
| [**Radiobutton**](radiobutton-control.md)         | Cria um controle de botão de opção.                                             |
| [**RTEXT**](rtext-control.md)                     | Cria um controle alinhado à direita.                                            |
| [**ROLAGEM**](scrollbar-control.md)             | Cria um controle de barra de rolagem.                                               |
| [**STATE3**](state3-control.md)                   | Cria um controle de caixa de seleção de três Estados.                                    |



 

## <a name="statements"></a>Instruções



| Instrução                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Legenda**](caption-statement.md)                 | Define o título de uma caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**CARACTERÍSTICAS**](characteristics-statement.md) | Especifica informações sobre um recurso que pode ser usado pela ferramenta que pode ler ou gravar arquivos de definição de recurso.                                                                                                                                                                                                                                                                                                                                                                           |
| [**CLASSES**](class-statement.md)                     | Define a classe da caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Comstyle**](exstyle-statement.md)                 | Define o estilo de janela estendida da caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**LA**](font-statement.md)                       | Define a fonte com a qual o sistema irá desenhar o texto para a caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**IDIOMA**](language-statement.md)               | Define o idioma para todos os recursos até a próxima instrução de [**idioma**](language-statement.md) ou para o final do arquivo. Quando a instrução de **idioma** aparece antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**diálogo**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , o idioma especificado aplica-se somente a esse recurso. |
| [**ADICIONARMENU**](menu-statement.md)                       | Define o menu para a caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MENUITEM**](menuitem-statement.md)               | Define um item de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ESTILO**](style-statement.md)                     | Define o estilo da janela para a caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Versão**](version-statement.md)                 | Especifica informações de versão para um recurso que pode ser usado pela ferramenta que pode ler ou gravar arquivos de definição de recurso.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 