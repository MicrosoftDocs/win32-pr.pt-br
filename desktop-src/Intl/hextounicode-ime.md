---
description: A edição avançada 3,0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso em uma de duas maneiras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506281"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

A edição avançada 3,0 dá suporte ao IME HexToUnicode, que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso em uma de duas maneiras.

Usando o primeiro método de conversão, o usuário digita o código de caractere em hexadecimal e, em seguida, insere ALT + X. O IME substitui os dígitos hexadecimais que antecedem o ponto de inserção com o caractere Unicode. Se a fonte atual não oferecer suporte ao código de caractere, será escolhida uma fonte apropriada que ofereça suporte a ela. Para converter de Unicode em hexadecimal, o usuário insere SHIFT + ALT + X. Essa entrada substitui o caractere Unicode que precede o ponto de inserção com os dígitos hexadecimais. Em particular, esse método permite que o usuário determine o caractere indicado por um indicador de "glifo ausente". Se o código de caractere hexadecimal seguir imediatamente alguns caracteres hexadecimais (não caracteres) legítimos, o usuário selecionará os dígitos específicos a serem convertidos antes de digitar ALT + X. Um problema com esse primeiro método é que ALT + X às vezes é usado como uma combinação de teclas para o comando exit (ou seja, eXit). Por exemplo, em Microsoft Office, esse comando só aparece como uma opção do menu **arquivo** .

O segundo método de conversão entre caracteres hexadecimais e Unicode envolve o teclado numérico. Usando esse método, o usuário digita ALT + números de teclado numérico (com valores maiores que 255) para inserir caracteres Unicode usando valores decimais. Esse método não é tão útil quanto o primeiro porque o usuário não pode ver quais dígitos hexadecimais foram digitados. Além disso, o usuário não pode corrigir os dígitos hexadecimais, exceto inserindo novamente todos os dígitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



