---
description: A cadeia de caracteres de composição é o texto atual na janela de composição.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Cadeia de caracteres de composição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a547b4383c95b99025b779de2950c8325af56a3397603db10199474dfe20ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430986"
---
# <a name="composition-string"></a>Cadeia de caracteres de composição

A cadeia de caracteres de composição é o texto atual na janela de composição. Esse é o texto que o IME converte para os caracteres finais. Cada cadeia de caracteres de composição consiste em uma ou mais "cláusulas". Uma cláusula é a menor combinação de caracteres que o IME pode converter em um caractere final. Para obter e definir a cadeia de caracteres de composição, o aplicativo chama as funções [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) , respectivamente.

Conforme o usuário digita o texto na janela de composição, o IME acompanha o status da cadeia de caracteres de composição. Esse status inclui informações de atributo, informações de cláusula, informações de digitação e posição do cursor. O aplicativo pode recuperar o status da composição usando a função [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) .

As informações de atributo são renderizadas em uma matriz de valores de 8 bits que especifica o status dos caracteres na cadeia de caracteres de composição. Todos os caracteres de uma cláusula devem ter o mesmo atributo. A matriz inclui um valor para cada byte na cadeia de caracteres, incluindo um byte cada para o cliente potencial e segundo bytes de qualquer caractere de byte duplo na cadeia de caracteres. Para cada valor na matriz, o bits 0 a 3 pode ser uma combinação dos valores a seguir.



| Valor                      | Significado                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| \_entrada attr                | Caractere que está sendo inserido pelo usuário. O IME ainda não converte esse caractere.                           |
| \_erro de entrada attr \_         | Um caractere de erro que o IME não pode converter. Por exemplo, o IME não pode reunir algumas consoantes. |
| \_destino attr \_ convertido    | Caractere selecionado pelo usuário e, em seguida, convertido pelo IME.                                             |
| ATTR \_ convertido            | Caractere que o IME já converteu.                                                             |
| destino ATTR não \_ \_ convertido | Caractere que está sendo convertido. O usuário selecionou esse caractere, mas o IME ainda não o converteu.     |
| \_FIXEDCONVERTED attr       | Caracteres que o IME não irá mais converter.                                                           |



 

Todos os outros valores são reservados. Em Japonês, qualquer caractere não convertido que tenha o \_ atributo de entrada attr é um caractere hiragana, Katakana ou alfanumérico. Em coreano, esse atributo representa um caractere hangul que o IME ainda não converteu. No chinês tradicional e no chinês simplificado, cada IME pode limitar seu caractere dentro de algum intervalo.

As informações de cláusula incluídas no status da cadeia de caracteres de composição são uma matriz de valores de 32 bits que especifica as posições das cláusulas na cadeia de caracteres de composição. A matriz inclui um valor para cada cláusula e um valor final que especifica o comprimento da cadeia de caracteres completa. Cada valor na matriz Especifica o deslocamento, em bytes, do início da cadeia de caracteres até a cláusula. O primeiro valor é sempre 0 porque a primeira cláusula sempre começa no início da cadeia de caracteres. Por exemplo, se uma cadeia de caracteres tiver duas cláusulas, as informações de cláusula têm três valores: o primeiro valor é 0, o segundo valor é o deslocamento da segunda cláusula e o terceiro valor é o comprimento da cadeia de caracteres. Para Unicode, a posição de uma cláusula é contada em caracteres Unicode e o comprimento de uma cadeia de caracteres é o tamanho em caracteres Unicode.

As informações de digitação incluídas no status da cadeia de caracteres de composição são uma cadeia de caracteres terminada em nulo que representa os caracteres que o usuário insere no teclado.

A posição do cursor incluída no status da cadeia de caracteres de composição é um valor que indica a posição do cursor em relação aos caracteres na cadeia de caracteres de composição. O valor é o deslocamento, em bytes, do início da cadeia de caracteres. Se esse valor for 0, o cursor será imediatamente antes do primeiro caractere na cadeia de caracteres. Se o valor for igual ao comprimento da cadeia de caracteres, o cursor será imediatamente após o último caractere. Se o valor for 1, o cursor não estará presente. Para Unicode, a posição e o comprimento são medidos em caracteres Unicode.

Seu aplicativo pode definir a cadeia de caracteres de composição ou os elementos do status da composição usando a função [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) . Para garantir que a janela de composição Atualize sua aparência com base nessas alterações, a função permite que o aplicativo envie uma mensagem de notificação para a janela. Os aplicativos que definem uma combinação de elementos de status de composição normalmente desabilitam as notificações para todas, exceto a última chamada para essa função, de forma que apenas uma mensagem de notificação seja gerada para a janela de composição.

Por fim, o controle de edição dá suporte a duas mensagens para alterar o tratamento de cadeias de caracteres de composição pelo IME. Para obter mais informações, consulte em [**\_ GETIMESTATUS**](../controls/em-getimestatus.md) e em [**\_ SETIMESTATUS**](../controls/em-setimestatus.md). Para obter mais informações sobre o controle de edição, consulte [Editar controle](../controls/edit-controls.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
