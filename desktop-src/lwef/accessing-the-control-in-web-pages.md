---
title: Acessando o controle em páginas da Web
description: Acessando o controle em páginas da Web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb6476ebdf2d26f1aec12a2f46506b3c4882d06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882970"
---
# <a name="accessing-the-control-in-web-pages"></a>Acessando o controle em páginas da Web

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para acessar os serviços do Microsoft Agent de uma página da Web, use a marca &lt; HTML OBJECT &gt; dentro do <HEAD> ou &lt; o elemento BODY da &gt; página, especificando a CLSID da Microsoft (identificador de classe) para o controle. Além disso, use um parâmetro CODEBASE para especificar o local do arquivo de instalação do Microsoft Agent e seu número de versão.

Se o Microsoft Internet Explorer (versão 3.02 ou posterior) estiver instalado no sistema, mas o Microsoft Agent ainda não estiver instalado e o usuário acessar uma página da Web que tenha a marca OBJECT com a CLSID do Agent, o navegador tentará baixar automaticamente o Agent do site &lt; &gt; da Microsoft. Em seguida, o usuário será perguntado se deve prosseguir com a instalação. Para outros navegadores, entre em contato com o fornecedor para obter informações sobre seu suporte ou suporte de terceiros para ActiveX controles.

O exemplo a seguir ilustra como usar o parâmetro CODEBASE para fazer o download automático do idioma inglês versão 2.0 do Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

O Agent também pode ser instalado do seu próprio servidor HTTP ou como parte do processo de instalação de um aplicativo. Para dar suporte à instalação do seu próprio servidor HTTP, você precisa postar o arquivo de gabinete de auto-instalação do Microsoft Agent .Exe e especificar sua URL na marca CODEBASE.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Para dar suporte ao download automático de um componente de linguagem do Microsoft Agent de uma página da Web, inclua a marca object do componente de linguagem na página antes da marca de objeto de controle do Agente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

em que XXXX é substituído por uma ID de linguagem. Para os idiomas com suporte no momento, verifique o site do Microsoft Agent.

-   A &lt; marca OBJECT de um componente de linguagem deve &gt; preceder a marca OBJECT para o &lt; componente principal do Microsoft &gt; Agent.
-   Vários idiomas podem ser instalados no mesmo cliente.
-   Antes de definir [**o LanguageID**](https://www.bing.com/search?q=**LanguageID**) de um caractere, recomendamos que o script verifique se a localidade do navegador, disponível na [**propriedade userLanguage,**](https://www.bing.com/search?q=**userLanguage**) corresponde ao idioma que está sendo definido.

Para dar suporte a outras versões de idioma do Agent, use outra marca object especificando o componente de linguagem. No entanto, esteja ciente de que tentar instalar vários idiomas ao mesmo tempo pode exigir que o usuário reinicialize. Os componentes de linguagem do Agent podem ser obtidos do site do Agent usando o mesmo procedimento do componente principal do Agent. O licenciamento de distribuição para os componentes de linguagem é abordado na licença de distribuição do Agent padrão. Para começar a usar um caractere, você deve carregar o caractere usando o [**método**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) Load. Um caractere pode ser carregado do armazenamento local do usuário ou de um servidor HTTP. Para obter mais informações sobre a sintaxe para carregar um caractere, consulte o **método Load.** Depois que o caractere tiver sido carregado com êxito, você poderá usar os métodos, propriedades e eventos expostos pelo controle Agent para programar o caractere. Você também pode usar os métodos, propriedades e eventos expostos pela linguagem de programação e pelo navegador para programar o caractere; por exemplo, para programar sua reação a um clique de botão. Consulte a documentação do navegador para determinar quais recursos ele expõe em seu modelo de script. Para o Microsoft Internet Explorer, consulte o Modelo de Objeto de Script, que está disponível no SDK do ActiveX.

Os serviços do agent permanecem carregados somente quando há pelo menos um aplicativo cliente com uma conexão. Isso significa que quando um usuário se move entre páginas da Web habilitadas para Agente, o Agent será desligado e todos os caracteres carregados desaparecerão. Para manter o Agent em execução entre as páginas (e, assim, manter um caractere visível), crie outro cliente que permaneça carregado entre as alterações de página. Por exemplo, você pode criar um quadro HTML e declarar uma &lt; marca OBJECT para Agent no quadro &gt; pai. Em seguida, você pode fazer o script das páginas carregadas nos quadros filho para chamar o script do pai. Como alternativa, você também pode incluir uma &lt; marca OBJECT em cada página carregada no quadro &gt; filho. Nesse caso, lembre-se de que cada página será seu próprio cliente. Talvez seja necessário usar o método [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) para definir qual cliente tem controle quando o usuário interage com a página pai ou filho.

 

 
