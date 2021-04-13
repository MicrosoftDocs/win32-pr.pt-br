---
description: Um vetor de versão processa comentários condicionais em uma página da Web HTML. Ou seja, os vetores de versão permitem criar marcação com base na versão do navegador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vetores da Versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297758"
---
# <a name="version-vectors"></a>Vetores da Versão

Um *vetor de versão* processa comentários condicionais em uma página da Web HTML. Ou seja, os vetores de versão permitem criar marcação com base na versão do navegador.

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



Nesse caso, se a versão do navegador do Windows Internet Explorer for pelo menos 5,5, o parágrafo correspondente será exibido na página da Web. Embora a primeira condição neste exemplo ilustre a função de comentários condicionais, esses comentários não são normalmente usados para exibir marcação como a primeira condição. Em vez disso, os comentários condicionais restantes no exemplo anterior são mais comuns. Nesses comentários restantes, os comentários condicionais usam uma folha de estilos diferente para cada versão diferente do navegador.

O exemplo de código anterior também verifica a igualdade do Microsoft Internet Explorer 6 e do Windows Internet Explorer 7. Mas, para o Windows Internet Explorer 8, o exemplo usa o operador GTE (maior ou igual). Esse operador ajuda a verificar o futuro o exemplo de forma que a versão em conformidade com os padrões da folha de estilos seja usada quando uma nova versão do navegador for liberada (em vez de usar a folha de estilos incorreta ou nenhuma folha de estilos). Os aplicativos existentes geralmente não consideram uma versão do Internet Explorer anterior 7 (ou a versão mais recente do Internet Explorer para a qual o site é criado). Para obter mais informações sobre os vetores de versão, consulte [vetores de versão](/previous-versions/cc817577(v=msdn.10)) na biblioteca MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



