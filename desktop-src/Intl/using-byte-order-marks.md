---
description: Sempre Prefixe um arquivo de texto sem formatação Unicode com uma marca de ordem de byte, que informa a um aplicativo que está recebendo o arquivo que o arquivo é ordenado por byte.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Usando marcas de ordem de byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747354"
---
# <a name="using-byte-order-marks"></a>Usando marcas de ordem de byte

Sempre Prefixe um arquivo de texto sem formatação Unicode com uma marca de ordem de byte, que informa a um aplicativo que está recebendo o arquivo que o arquivo é ordenado por byte. As marcas de ordem de byte disponíveis são listadas na tabela a seguir. Como o texto sem formatação Unicode é uma sequência de valores de código de 16 bits, ele é sensível à ordenação de bytes usada quando o texto é gravado.

> [!Note]  
> Uma marca de ordem de byte não é um caractere de controle que seleciona a ordem de bytes do texto.

 



| Marca de ordem de byte | Descrição           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16, little endian |
| FF DE FE           | UTF-16, big endian    |
| FF FE 00 00     | UTF-32, little endian |
| 00 00 FE FF     | UTF-32, big-endian    |



 

> [!Note]  
> A Microsoft usa a ordem UTF-16, little endian byte.

 

O ideal é que todo o texto Unicode Siga apenas um conjunto de regras de ordenação de bytes. No entanto, isso não é possível porque os microprocessadores diferem no posicionamento do byte menos significativo. Os processadores Intel e MIPS posicionam o byte menos significativo primeiro, enquanto os processadores Motorola (e todos os arquivos Unicode invertidos em bytes) o posicionam por último. Com apenas um conjunto único de regras de ordenação de bytes, os usuários de um tipo de microprocessador são forçados a trocar a ordem de bytes sempre que um arquivo de texto sem formatação é lido ou gravado, mesmo que o arquivo nunca seja transferido para outro sistema operacional com base em um microprocessador diferente.

O local preferencial para especificar a ordem de byte está em um cabeçalho de arquivo, mas os arquivos de texto não têm cabeçalhos. Portanto, o Unicode definiu um caractere (U + FEFF) e um não caractere (U + FFFE) como marcas de ordem de byte. Elas são imagens de byte espelhadas uma da outra.

Como a sequência U + FEFF é extremamente rara no início de um arquivo de texto não-Unicode regular, ele pode servir como um marcador ou assinatura implícita para identificar o arquivo como um arquivo Unicode. Os aplicativos que lêem arquivos de texto Unicode e não Unicode devem usar a presença dessa sequência como um indicador de que o arquivo provavelmente é um arquivo Unicode. Compare essa técnica com o uso do marcador EOF do MS-DOS para encerrar arquivos de texto.

Quando um aplicativo encontra U + FEFF no início de um arquivo de texto, ele normalmente processa o arquivo como um arquivo Unicode, embora possa executar verificações de heurística adicionais para verificação. Essa verificação pode ser tão simples quanto o teste para descobrir se a variação nos bytes de ordem inferior é muito maior do que a variação nos bytes de ordem superior. Por exemplo, se o texto ASCII for convertido em texto Unicode, cada segundo byte será 0. Além disso, a verificação dos caracteres de alimentação e de retorno de carro (U + 000A e U + 000D) e de tamanho de arquivo par ou ímpar pode fornecer um indicador forte da natureza do arquivo.

Quando um aplicativo encontra U + FFFE no início de um arquivo de texto, ele o interpreta para significar que o arquivo é um arquivo Unicode invertido em bytes. O aplicativo pode trocar a ordem dos bytes ou alertar o usuário de que ocorreu um erro.

Como o caractere de marca de ordem de byte Unicode não é encontrado em nenhuma página de código, ele desaparece se os dados são convertidos em ANSI. Ao contrário de outros caracteres Unicode, ele não é substituído por um caractere padrão quando é convertido. Se uma marca de ordem de byte for encontrada no meio de um arquivo, ela não será interpretada como um caractere Unicode e não terá nenhum efeito na saída de texto.

> [!Note]  
> O valor Unicode U + FFFF é inválido em arquivos de texto sem formatação e não pode ser passado entre aplicativos. Ele é reservado para o uso particular de um aplicativo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



