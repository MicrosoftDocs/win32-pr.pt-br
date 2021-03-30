---
title: Acessando o controle em páginas da Web
description: Acessando o controle em páginas da Web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a965d73f7277b2b4a62c08a949782488f1e4dba4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640572"
---
# <a name="accessing-the-control-in-web-pages"></a>Acessando o controle em páginas da Web

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para acessar os serviços do Microsoft Agent de uma página da Web, use a <OBJECT> marca HTML dentro do <HEAD> ou <BODY> elemento da página, especificando o Microsoft CLSID (identificador de classe) para o controle. Além disso, use um parâmetro CODEBASE para especificar o local do arquivo de instalação do Microsoft Agent e seu número de versão.

Se o Microsoft Internet Explorer (versão 3, 2 ou posterior) estiver instalado no sistema, mas o agente da Microsoft ainda não estiver instalado e o usuário acessar uma página da Web que tenha a <OBJECT> marca com o CLSID do agente, o navegador tentará automaticamente baixar o agente do site da Microsoft. Em seguida, o usuário será perguntado se deseja prosseguir com a instalação. Para outros navegadores, entre em contato com o fornecedor para obter informações sobre seu suporte ou suporte de terceiros para controles ActiveX.

O exemplo a seguir ilustra como usar o parâmetro CODEBASE para baixar o idioma em inglês versão 2,0 do Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

O Agent também pode ser instalado de seu próprio servidor HTTP ou como parte do processo de instalação de um aplicativo. Para dar suporte à instalação de seu próprio servidor HTTP, você precisa postar o gabinete de instalação automática do Microsoft Agent. Arquivo exe e especifique sua URL na marca CODEBASE.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Para dar suporte ao download automático de um componente de linguagem do Microsoft Agent de uma página da Web, inclua a marca de objeto do componente de idioma na página antes da marca do objeto de controle do agente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

em que XXXX é substituído por uma ID de idioma. Para os idiomas com suporte no momento, verifique o site do Microsoft Agent.

-   A <OBJECT> marca para um componente de linguagem deve preceder a <OBJECT> marca para o componente principal do Microsoft Agent.
-   Vários idiomas podem ser instalados no mesmo cliente.
-   Antes de definir [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) de um caractere, recomendamos que o script Verifique se a localidade do navegador, disponível na propriedade [**UserLanguage**](https://www.bing.com/search?q=**userLanguage**) , corresponde ao idioma que está sendo definido.

Para dar suporte a outras versões de idioma do Agent, use outra marca de objeto especificando o componente de idioma. No entanto, lembre-se de que a tentativa de instalar vários idiomas ao mesmo tempo pode exigir que o usuário seja reinicializado. Os componentes de idioma do agente podem ser obtidos no site do agente usando o mesmo procedimento do componente principal do agente. O licenciamento de distribuição para os componentes de linguagem é abordado na licença de distribuição de agente padrão. Para começar a usar um caractere, você deve carregar o caractere usando o método [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) . Um caractere pode ser carregado do armazenamento local do usuário ou de um servidor HTTP. Para obter mais informações sobre a sintaxe para carregar um caractere, consulte o método **Load** . Depois que o caractere tiver sido carregado com êxito, você poderá usar os métodos, as propriedades e os eventos expostos pelo controle do agente para programar o caractere. Você também pode usar os métodos, as propriedades e os eventos expostos pela sua linguagem de programação e o navegador para programar o caractere; por exemplo, para programar sua reação a um clique de botão. Consulte a documentação do seu navegador para determinar quais recursos ele expõe em seu modelo de script. Para o Microsoft Internet Explorer, consulte o modelo de objeto de script, que está disponível no SDK do ActiveX.

Os serviços do agente permanecem carregados somente quando há pelo menos um aplicativo cliente com uma conexão. Isso significa que, quando um usuário se move entre páginas da Web habilitadas para agente, o agente é desligado e os caracteres que você carregou desaparecerão. Para manter o agente em execução entre as páginas (e, portanto, manter um caractere visível), crie outro cliente que permanece carregado entre as alterações de página. Por exemplo, você pode criar um conjunto de quadros HTML e declarar uma <OBJECT> marca para o Agent no quadro pai. Em seguida, você pode criar um script das páginas que carrega no (s) quadro (es) filho para chamar o script do pai. Como alternativa, você também pode incluir uma <OBJECT> marca em cada página carregada no quadro filho. Nesse caso, lembre-se de que cada página será seu próprio cliente. Talvez seja necessário usar o método [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) para definir qual cliente tem controle quando o usuário interage com a página pai ou filho.

 

 