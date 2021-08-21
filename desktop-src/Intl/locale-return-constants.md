---
description: Constantes \_ RETURN \* LOCALE
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: constantes LOCALE_RETURN*
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466023"
---
# <a name="locale_return-constants"></a>Constantes \_ RETURN \* LOCALE

Este tópico define as \_ constantes RETURN LOCALE \* usadas pelo NLS.




| Valor | Significado | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 e posteriores:</strong> Recupere os nomes genitivos de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens. Por exemplo, em Igual a Janeiro, o equivalente a janeiro é escrito "Ão" quando o mês é nomeado sozinho. No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitiva do nome é usada. Para o exemplo Desaloque, o nome do mês genitivo é exibido como "5 º º 2003". A lista de nomes de mês genitive começa em janeiro e é delimitada por ponto e vírgula. Se não houver 13º mês, use um ponto e vírgula em seu lugar no final da lista.<blockquote>[!Note]<br />Nomes de mês genitivo não existem em todos os idiomas.</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98, Windows NT 4.0 e posterior:</strong> Recuperar um número. Essa constante faz <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>com que GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperem um valor como um número em vez de como uma cadeia de caracteres. O buffer que recebe o valor deve ter pelo menos o comprimento de um valor DWORD. Essa constante pode ser combinada com qualquer outra constante que tenha um nome que comece com "LOCALE_I". | 




 

 

 




