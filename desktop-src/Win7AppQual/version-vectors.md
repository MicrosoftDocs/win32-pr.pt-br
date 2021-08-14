---
description: Um vetor de versão processa comentários condicionais em uma página da Web HTML. Ou seja, os vetores de versão permitem que você crie marcação com base na versão do navegador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vetores da Versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ba3fb77d13ce6aa08a095f4ae95e88c1ffaecf57251b7d9ad718f51be3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328602"
---
# <a name="version-vectors"></a>Vetores da Versão

Um *vetor de* versão processa comentários condicionais em uma página da Web HTML. Ou seja, os vetores de versão permitem que você crie marcação com base na versão do navegador.

Considere o exemplo de código a seguir.


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



Nesse caso, se a Windows Internet Explorer do navegador for pelo menos 5.5, o parágrafo correspondente será exibido na página da Web. Embora a primeira condição neste exemplo ilustra a função de comentários condicionais, esses comentários normalmente não são usados para exibir marcação como a primeira condição. Em vez disso, os comentários condicionais restantes no exemplo anterior são mais comuns. Nesses comentários restantes, os comentários condicionais usam uma folha de estilos diferente para cada versão diferente do navegador.

O exemplo de código anterior também verifica a igualdade para o Microsoft Internet Explorer 6 e Windows Internet Explorer 7. Mas, Windows Internet Explorer 8, o exemplo usa o operador gte (maior ou igual). Esse operador ajuda o exemplo à prova de futuro para que a versão mais em conformidade com os padrões da folha de estilos seja usada quando uma nova versão do navegador for liberada (em vez de usar a folha de estilos errada ou nenhuma folha de estilos). Os aplicativos existentes geralmente não consideram uma versão do Internet Explorer 7 (ou a versão mais recente do Internet Explorer para a que o site foi criado). Para obter mais informações sobre vetores de versão, consulte [Vetores de](/previous-versions/cc817577(v=msdn.10)) versão no Biblioteca MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



