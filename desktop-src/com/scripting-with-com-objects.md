---
title: Criando scripts com objetos COM
description: Criando scripts com objetos COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2019
ms.locfileid: "103638290"
---
# <a name="scripting-with-com-objects"></a>Criando scripts com objetos COM

Uma *linguagem de script* é uma linguagem de programação analisada em tempo de execução por um *mecanismo de script*, um componente que traduz scripts escritos nesse idioma no código da máquina. Cada mecanismo de script converte uma linguagem de script específica. Um *host de script* é um aplicativo, como um navegador da Web, que hospeda um mecanismo de script para executar scripts. Se o seu host de script oferecer suporte a COM, você poderá escrever scripts que usam objetos COM. Os tópicos a seguir descrevem os hosts de script que dão suporte a objetos COM, linguagens de script comuns e como converter entre linguagens de script.

Uma linguagem de script difere de uma linguagem compilada, pois ela é traduzida no código do computador em tempo de execução. Isso significa que sempre que você executar um script, o mecanismo de script primeiro analisa o código e, em seguida, executa-o. Por outro lado, linguagens compiladas, como C++, são convertidas no código do computador uma vez, durante a compilação. Quando você executa um aplicativo compilado, o sistema operacional simplesmente executa o código pré-compilado.

Como um mecanismo de script deve analisar novamente um script cada vez que ele é executado, as linguagens de script são normalmente mais lentas e menos eficientes do que suas contrapartes pré-compiladas. No entanto, a vantagem dos scripts é fácil de escrever e manter. As linguagens de script são geralmente mais simples do que linguagens pré-compiladas e, quando um script é alterado, ele não precisa ser recompilado. Para aplicativos simples e de alteração rápida, como páginas da Web, linguagens de script são ideais.

Há vários ambientes de host nos quais você pode gravar scripts que usam objetos COM, conforme descrito a seguir:

-   [Inserindo objetos COM em páginas da Web](embedding-com-objects-in-web-pages.md)
-   [Usando objetos COM em páginas Active Server](using-com-objects-in-active-server-pages.md)
-   [Usando objetos COM no Windows Script Host](using-com-objects-in-windows-script-host.md)
-   [Criando scripts de objetos COM em aplicativos personalizados](scripting-com-objects-in-custom-applications.md)

Em cada um dos ambientes de host mencionados anteriormente, um mecanismo de script analisa e executa o script. Como o mecanismo de cada linguagem de script é um componente separado, você pode adicionar uma nova linguagem de script a um ambiente adicionando um novo mecanismo.

As linguagens de script usadas com mais frequência são:

-   O Microsoft Visual Basic Scripting Edition (VBScript), um subconjunto de Visual Basic.
-   JavaScript, a linguagem de script do Netscape, anteriormente conhecida como LiveScript.
-   Software de desenvolvimento Microsoft JScript, a implementação da Microsoft da especificação da linguagem ECMA 262.

A Microsoft fornece mecanismos de script para JScript e VBScript. Outras empresas de software fornecem mecanismos de script do ActiveX para linguagens como PerlScript, PScript, Python e outros.

Para obter mais informações, consulte a [especificação da linguagem ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Observe que a maioria das linguagens de script, como VBScript e JScript, não pode acessar ou modificar arquivos. Essa incapacidade impede que o script altere os dados nos computadores cliente. No entanto, objetos COM não têm essas limitações. Depois que eles são baixados e instalados nos computadores cliente, eles podem executar qualquer ação padrão do aplicativo. Portanto, os usuários só devem baixar e executar controles ActiveX de fontes confiáveis.

Para obter informações sobre a tradução entre linguagens de script, consulte os seguintes tópicos:

-   [Convertendo para VBScript](translating-to-vbscript.md)
-   [Traduzindo para o JScript](translating-to-jscript.md)
-   [Convertendo para JavaScript](translating-to-javascript.md)

 

 




