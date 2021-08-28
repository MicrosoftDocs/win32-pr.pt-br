---
description: Os aplicativos escrevem caracteres definidos pelo usuário final (EUDCs) e caracteres PUA (área de uso privado) na tela ou impressora, assim como escrevem outros caracteres, usando funções de saída como TextOut e ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Escrevendo, mapeando e classificação de caracteres EUDC e PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ab43eb54055b97fe1823ad99467a4cd0b12a0a5fb971d52d225631cfd37ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102076"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Escrevendo, mapeando e classificação de caracteres EUDC e PUA

Os aplicativos escrevem caracteres definidos pelo usuário final (EUDCs) e caracteres PUA (área de uso privado) na tela ou impressora, assim como escrevem outros caracteres, usando funções de saída como [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) e [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Essas funções recuperam automaticamente informações de caractere de fontes de caracteres EUDC ou PUA se o EUDC estiver habilitado. Para obter mais informações, consulte Caracteres de área de uso privado e [ \_ definidos pelo usuário final.](end-user-defined-characters.md)

Ao escrever caracteres EUDCs ou PUA, a operação da função de saída de texto depende da fonte selecionada no momento. Se a fonte selecionada for uma fonte de caracteres EUDC ou PUA integrada, a função recuperará informações de caractere dessa fonte. Se a fonte selecionada for uma fonte TrueType DBCS (conjunto de caracteres de dois [byte)](double-byte-character-sets.md) que tenha uma fonte EUDC separada associada, a função recuperará informações da fonte EUDC especificada. Da mesma forma, se a fonte selecionada for uma [fonte TrueType Unicode](unicode.md) que tenha uma fonte de caractere PUA separada associada, a função recuperará informações da fonte de caracteres PUA. Se a fonte selecionada não tiver uma fonte de caracteres EUDC ou PUA associada, a função recuperará informações da fonte EUDC padrão do sistema. Se o caractere não estiver na fonte EUDC padrão do sistema ou não houver nenhuma fonte EUDC padrão do sistema, a função grava o caractere padrão definido pela fonte selecionada.

Os aplicativos podem mapear EUDCs de e para Unicode usando as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte.**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) A **função MultiByteToWideChar** mapeia a maioria dos EUDCs para caracteres na PUA Unicode. No entanto, para dar suporte a determinados padrões nacionais ou regionais, alguns EUDCs podem ser mapeados para pontos de código Unicode não PUA. A **função WideCharToMultiByte** mapeia um caractere no PUA para sua contraparte do EUDC, se esse mapeamento existir e se o ponto de código não tiver um mapeamento não PUA válido em Unicode. Nem todas as páginas de código têm um intervalo de EUDC. A página de código especificada em uma chamada para **WideCharToMultiByte** deve conter um intervalo de código EUDC para que o mapeamento para o intervalo de EUDC ocorra. Se a página de código não contém um intervalo de código EUDC, a função recupera o caractere padrão para qualquer caractere no PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) não garantem o mapeamento de ida e volta. Em outras palavras, é possível começar com uma cadeia de caracteres multibyte específica que contém EUDCs, mapear a cadeia de caracteres para Unicode com **MultiByteToWideChar** e mapeá-la de volta para o DBCS original com **WideCharToMultiByte** e acabar com um resultado que não é idêntico à cadeia de caracteres original. Os aplicativos que dependem do mapeamento de EUDCs para Unicode devem garantir que todos os caracteres necessários possam fazer uma viagem de ida e volta entre a área de EUDC da página de código apropriada e a PUA Unicode.

Os aplicativos não devem tentar mapear EUDCs de uma página de código para outra. Se um aplicativo começar com um EUDC de uma página de código, o mapeia para Unicode com [**MultiByteToWideChar e**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)mapeia para um DBCS diferente com [**WideCharToMultiByte,**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)não há nenhuma garantia sobre os resultados. O caractere original pode ser mapeado para um EUDC diferente na página de código de destino ou pode ser mapeado como um caractere indefinido. Da mesma forma, mapear uma cadeia de caracteres Unicode para uma página de código que tem um intervalo euDC pode ter resultados não intencionais. Se a cadeia de caracteres Unicode contiver um ponto de código PUA, é possível que o ponto de código seja mapeado para um EUDC que não representa o mesmo caractere.

Os aplicativos podem comparar cadeias de caracteres DBCS que contêm EUDCs usando a versão ANSI da [função CompareString.](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) A função mapeia efetivamente os caracteres para Unicode antes de comparar valores de caracteres. Os aplicativos podem criar uma chave de classificação para a cadeia de caracteres usando a versão ANSI da função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) e o valor SORTKEY do \_ LCMAP. Essa função mapeia efetivamente os caracteres para Unicode primeiro. Todos os caracteres no PUA são classificação após todos os outros caracteres Unicode. Dentro da área, os caracteres são classificação em ordem numérica. Se um aplicativo tentar recuperar informações CTYPE para um EUDC usando a [função GetStringTypeA,](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) a função recuperará **NULL** para cada caractere.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
