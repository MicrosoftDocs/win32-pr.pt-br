---
title: Registrando um item de menu de contexto estático
description: Este tópico descreve o registro de um item de menu de contexto estático exibido para objetos Active Directory.
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Registrando um item de menu de contexto estático AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e3ee5336061ca296e2c94f8907ebd385610494
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105753873"
---
# <a name="registering-a-static-context-menu-item"></a>Registrando um item de menu de contexto estático

Os snap-ins administrativos do MMC do Active Directory Domain Services e do shell do Windows fornecem um mecanismo para adicionar um item ao menu de contexto exibido para objetos no Active Directory Domain Services. O menu de contexto pode invocar qualquer arquivo que possa ser iniciado com a API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como uma URL do aplicativo ou da página da Web.

## <a name="registering-with-active-directory-domain-services"></a>Registrando com Active Directory Domain Services

O registro de extensão do menu de contexto é específico para uma localidade. Se a extensão do menu de contexto se aplicar a todas as localidades, ela deverá ser registrada no objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) da classe Object em todos os subcontêineres de localidade no contêiner exibir especificadores. Se a extensão do menu de contexto for localizada para uma determinada localidade, ela deverá ser registrada no objeto **displaySpecifier** nesse subcontêiner de localidade. Para obter mais informações sobre o contêiner e as localidades dos especificadores de exibição, consulte [Exibir especificadores de exibição](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).

Há dois atributos de especificador de exibição em que um item de menu de contexto estático pode ser registrado, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

O atributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica os menus de contexto administrativos a serem exibidos nos snap-ins administrativos de Active Directory Domain Services. O menu de contexto é exibido quando o usuário exibe o menu de contexto para objetos da classe apropriada em um dos snap-ins administrativos do MMC.

O atributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica os menus de contexto do usuário final a serem exibidos no Shell do Windows. O menu de contexto é exibido quando o usuário exibe o menu de contexto para objetos da classe apropriada no Windows Explorer. A partir do Windows Server 2003, o Shell do Windows não exibe mais objetos do Active Directory Domain Services.

Todos esses atributos têm valores múltiplos.

Ao registrar um item de menu de contexto estático, os valores para os atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) exigem o formato a seguir.


```C++
<order number>,<menu text>,<command>
```



O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição do item no menu de contexto. Quando um menu de contexto é exibido, os valores são classificados usando uma comparação de "número de &lt; ordem" de cada valor &gt; . Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", essas extensões de menu de contexto serão carregadas na ordem em que são lidas do servidor de Active Directory. Se possível, use um " &lt; número de pedido" não existente &gt; , ou seja, um que não tenha sido usado por outros valores na propriedade. Não há uma posição de início prescrita e as lacunas são permitidas na &lt; sequência "número do pedido &gt; ".

O " &lt; texto do menu &gt; " é a cadeia de caracteres exibida no menu de contexto. O " &lt; texto do menu &gt; " pode incluir um caractere "&" que precede o caractere de atalho do teclado para o item de menu. Isso fará com que o caractere precedido seja sublinhado. Por exemplo, se o " &lt; texto do menu &gt; " for "&arquivo", o texto do menu será exibido como "arquivo", o "f" será sublinhado e "f" será o atalho do teclado para o item de menu.

O " &lt; comando &gt; " é o programa ou arquivo executado pelo snap-in do. O caminho completo deve ser especificado ou o arquivo deve existir na variável de ambiente Path do computador. O arquivo é invocado usando a função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) . O " &lt; comando &gt; " não pode conter parâmetros adicionais, por exemplo, Notepad.exe Myfile.txt. Como **ShellExecute** é usado, qualquer arquivo ou endereço que possa ser passado para **ShellExecute** pode ser usado para " &lt; Command &gt; ". Por exemplo, se " &lt; Command &gt; " contiver "d: \\file.txt", d: \\file.txt será aberto com o aplicativo associado à extensão. txt. Da mesma forma, se " &lt; Command &gt; " contiver " https://www.fabrikam.com ", o navegador da Web padrão será aberto e exibirá a página a seguir especificada. Caminhos e nomes de aplicativos com espaços são permitidos. Se " &lt; Command &gt; " for um aplicativo, o ADsPath e a classe do objeto selecionado serão passados como argumentos de linha de comando, separados por um espaço.

No Shell do Windows, há suporte para itens de menu de contexto de seleção múltipla. Nesse caso, o " &lt; comando &gt; " é invocado para cada objeto selecionado. Em Active Directory Domain Services ' snap-ins administrativos, não há suporte para itens de menu de contexto estático de seleção múltipla.

> [!IMPORTANT]
> Para o Shell do Windows, os dados do especificador de exibição são recuperados no logon do usuário e armazenados em cache para a sessão do usuário. Para os snap-ins administrativos, os dados do especificador de exibição são recuperados quando o snap-in é carregado e armazenado em cache durante a duração do processo. Para o Shell do Windows, isso significa que as alterações para os especificadores de exibição entram em vigor após o usuário fazer logoff e logon novamente. Para os snap-ins administrativos, as alterações entram em vigor quando o snap-in ou o arquivo de console é recarregado; ou seja, se você iniciar uma nova instância do arquivo de console ou nova instância de Mmc.exe e adicionar o snap-in, os dados do especificador de exibição mais recentes serão recuperados.

 

Para obter mais informações e um exemplo de código, consulte [código de exemplo para instalar um item de menu de contexto estático](example-code-for-installing-a-static-context-menu-item.md).

 

 