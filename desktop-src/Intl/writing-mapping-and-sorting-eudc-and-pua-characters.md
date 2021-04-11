---
description: Os aplicativos gravam EUDC (caracteres definidos pelo usuário final) e caracteres PUA (área de uso particular) na tela ou impressora, assim como gravam outros caracteres, usando funções de saída como TextOut e ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Gravando, mapeando e classificando os caracteres EUDC e PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164511"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Gravando, mapeando e classificando os caracteres EUDC e PUA

Os aplicativos gravam EUDC (caracteres definidos pelo usuário final) e caracteres PUA (área de uso particular) na tela ou impressora, assim como gravam outros caracteres, usando funções de saída como [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) e [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Essas funções recuperam automaticamente informações de caractere de fontes de caracteres EUDC ou PUA se o EUDC estiver habilitado. Para obter mais informações, consulte [caracteres da \_ área de uso privado e definido pelo usuário final](end-user-defined-characters.md).

Ao gravar EUDCs ou PUA caracteres, a operação da função de saída de texto depende da fonte atualmente selecionada. Se a fonte selecionada for uma fonte de caractere PUA ou EUDC integrada, a função recuperará informações de caractere dessa fonte. Se a fonte selecionada for uma fonte TrueType de [conjunto de caracteres de byte duplo](double-byte-character-sets.md) (DBCS) que tenha uma fonte EUDC separada associada, a função recuperará informações da fonte EUDC especificada. Da mesma forma, se a fonte selecionada for uma fonte TrueType [Unicode](unicode.md) que tem uma fonte de caracteres pua separada associada, a função recuperará informações da fonte de caracteres pua. Se a fonte selecionada não tiver uma fonte de caractere EUDC ou PUA associada, a função recuperará informações da fonte EUDC padrão do sistema. Se o caractere não estiver na fonte EUDC padrão do sistema ou não houver nenhuma fonte EUDC padrão do sistema, a função gravará o caractere padrão definido pela fonte selecionada.

Os aplicativos podem mapear EUDCs de e para o Unicode usando as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) . A função **MultiByteToWideChar** mapeia a maioria das EUDCs para caracteres no pua Unicode. No entanto, para dar suporte a determinados padrões nacionais ou regionais, algumas EUDCs podem ser mapeadas para pontos de código Unicode não PUA. A função **WideCharToMultiByte** mapeia um caractere no pua para sua contraparte EUDC, se esse mapeamento existir e se o ponto de código não tiver um mapeamento não pua válido em Unicode. Nem todas as páginas de código têm um intervalo EUDC. A página de código especificada em uma chamada de **WideCharToMultiByte** deve conter um intervalo de códigos EUDC para que o mapeamento para o intervalo Eudc ocorra. Se a página de código não contiver um intervalo de códigos EUDC, a função recuperará o caractere padrão para todos os caracteres no PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) não garantem o mapeamento de ida e volta. Em outras palavras, é possível iniciar com uma cadeia de caracteres multibyte específica contendo EUDCs, mapear a cadeia de caracteres para Unicode com **MultiByteToWideChar** e mapeá-la de volta para o DBCS original com **WideCharToMultiByte** e terminar com um resultado que não seja idêntico à cadeia de caracteres original. Os aplicativos que dependem do mapeamento de EUDCs para Unicode devem garantir que todos os caracteres necessários possam fazer ida e volta entre a área de EUDC da página de código apropriada e o PUA Unicode.

Os aplicativos não devem tentar mapear EUDCs de uma página de código para outra. Se um aplicativo começa com um EUDC de uma página de código, o mapeia para Unicode com [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)e mapeia para um DBCS diferente com [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte), não há nenhuma garantia sobre os resultados. O caractere original pode ser mapeado para um EUDC diferente na página de código de destino ou pode ser mapeado como um caractere indefinido. Da mesma forma, o mapeamento de uma cadeia de caracteres Unicode para uma página de código que tenha um intervalo EUDC pode ter resultados indesejados. Se a cadeia de caracteres Unicode contiver um ponto de código PUA, é possível que o ponto de código seja mapeado para um EUDC que não represente o mesmo caractere.

Os aplicativos podem comparar cadeias de caracteres DBCS que contêm EUDCs usando a versão ANSI da função [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) . A função mapeia efetivamente os caracteres para Unicode antes de comparar valores de caracteres. Os aplicativos podem criar uma chave de classificação para a cadeia de caracteres usando a versão ANSI da função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) e o \_ valor de SORTKEY LCMAP. Essa função mapeia efetivamente os caracteres para Unicode primeiro. Todos os caracteres no PUA são classificados após todos os outros caracteres Unicode. Dentro da área, os caracteres são classificados em ordem numérica. Se um aplicativo tentar recuperar informações de CTYPE para um EUDC usando a função [GetStringTypeA](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) , a função recuperará **NULL** para cada caractere.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
