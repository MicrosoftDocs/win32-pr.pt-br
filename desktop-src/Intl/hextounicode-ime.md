---
description: O Rich Edit 3.0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso de duas maneiras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a57ce56821f200c9fd9ff80560908f5a72ecfdb0f51ce981e1aff40ce785b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068146"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

O Rich Edit 3.0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso de duas maneiras.

Usando o primeiro método de conversão, o usuário digita o código de caractere em hexadecimal e, em seguida, entra em ALT+X. O IME substitui os dígitos hexadecimais anteriores ao ponto de inserção pelo caractere Unicode. Se a fonte atual não dá suporte ao código de caractere, uma fonte apropriada é escolhida que dá suporte a ela. Para converter de Unicode em hexadecimal, o usuário ins insinte shift+ALT+X. Essa entrada substitui o caractere Unicode que precede o ponto de inserção com os dígitos hexadecimais. Em particular, esse método permite que o usuário determine o caractere indicado por um indicador de "glifo ausente". Se o código de caractere hexadecimal seguir imediatamente alguns caracteres hexadecimais (não caracteres) legítimos, o usuário selecionará os dígitos específicos a converter antes de digitar ALT+X. Um problema com esse primeiro método é que ALT+X às vezes é usado como uma combinação de chaves para o comando exit (ou seja, eXit). Por exemplo, no Microsoft Office, esse comando aparece apenas como uma opção **do** menu Arquivo.

O segundo método de conversão entre caracteres hexadecimais e Unicode envolve o painel de números. Usando esse método, o usuário digita números ALT+NumPad (com valores maiores que 255) para inserir caracteres Unicode usando valores decimais. Esse método não é tão útil quanto o primeiro porque o usuário não pode ver quais dígitos hexadecimais foram digitados. Além disso, o usuário não pode corrigir os dígitos hexadecimais, exceto inserindo todos os dígitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de Métodos de Entrada](about-input-method-manager.md)
</dt> </dl>

 

 



