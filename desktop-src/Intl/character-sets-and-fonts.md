---
description: Windows permite a definição local de caracteres não padrão em DBCSs (conjuntos de caracteres de dois byte) e Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Conjuntos de caracteres e fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068276"
---
# <a name="character-sets-and-fonts"></a>Conjuntos de caracteres e fontes

Windows permite a definição local de caracteres não padrão em DBCSs (conjuntos de caracteres de dois [byte)](double-byte-character-sets.md) e [Unicode.](unicode.md) Para um DBCS, esses caracteres não padrão são conhecidos como EUDC (caracteres definidos pelo usuário final). O Unicode fornece uma funcionalidade semelhante por meio de sua PUA (área de uso privado). Os aplicativos identificam um caractere especificado usando o valor de caractere DBCS ou Unicode associado.

Os valores de caractere DBCS que podem ser atribuídos dependem do conjunto de caracteres especificado. Cada página de código Windows [leste](code-pages.md) da Ásia tem pelo menos um intervalo de valores reservados para uso como EUDCs. Os intervalos são definidos pela chave do Registro [EUDCCodeRange.](eudccoderange.md) Os valores Unicode para essa finalidade sempre vêm da PUA Unicode, dos valores U+E000 a U+F8FF, U+F0000 para U+FFFFD e U+100000 a U+10FFFD.

Para criar um caractere EUDC ou PUA, o usuário escolhe um valor de caractere que está dentro do intervalo especificado e adiciona o [glifo](uniscribe-glossary.md) à fonte na entrada que corresponde a esse valor de caractere. O usuário cria o glifo usando um editor euDC ou usando um pacote de fontes comprado de um fornecedor de fontes. Qualquer fonte DBCS pode conter EUDCs e qualquer fonte Unicode pode conter caracteres PUA. A fonte será chamada de fonte EUDC/PUA "separada" se contiver apenas EUDCs. A fonte será uma fonte EUDC/PUA "integrada" se contiver caracteres padrão, bem como EUDCs.

A fonte EUDC/PUA padrão do sistema é uma fonte que o sistema operacional associa automaticamente a todas as fontes DBCS e Unicode, exceto as fontes que associaram explicitamente fontes EUDC/PUA. Os aplicativos configuram a fonte EUDC/PUA padrão do sistema definindo o valor do nome SystemDefaultEUDCFont na chave do Registro [EUDC.](eudc.md) Da mesma forma, os aplicativos podem associar fontes EUDC/PUA separadas às fontes correspondentes especificando um nome de fonte e um arquivo de fonte associado na chave EUDC. O sistema operacional sempre tenta primeiro encontrar o EUDC/PUA na fonte selecionada no momento. Se a fonte não for encontrada, o sistema operacional procura o caractere na fonte EUDC/PUA associada, se um tiver sido definido para a fonte selecionada no momento. Se ainda não for possível encontrar o caractere, o sistema operacional o procurará na fonte EUDC/PUA padrão do sistema.

As fontes TrueType podem ser instaladas como arquivos .ttf ou como arquivos .tte. Como o sistema operacional oculta arquivos .tte, os aplicativos não podem enumerar ou examinar as fontes instaladas usando funções de API GDI. Em muitos sistemas operacionais, a fonte EUDC/PUA padrão do sistema e as fontes EUDC/PUA separadas são instaladas como arquivos .tte. Aplicativos como editores EUDC e Painel de Controle devem usar entradas do Registro para adicionar, modificar e excluir essas fontes.

O uso de caracteres EUDC e PUA não preserva de forma confiável o significado em diferentes computadores ou conjuntos de caracteres. Consulte [Caracteres de área de](end-user-defined-characters.md) uso privado e definidos pelo usuário final para saber mais sobre o uso de caracteres EUDC e PUA.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Caracteres de área de uso privado e definidos pelo usuário final](end-user-defined-characters.md)
</dt> </dl>

 

 



