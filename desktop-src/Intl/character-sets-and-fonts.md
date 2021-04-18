---
description: O Windows permite a definição local de caracteres não padrão em conjuntos de caracteres de dois bytes (DBCS) e Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Fontes e conjuntos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbf3dae2875ec6d714419bb45411f3208bfe5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770205"
---
# <a name="character-sets-and-fonts"></a>Fontes e conjuntos de caracteres

O Windows permite a definição local de caracteres não padrão em [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) (DBCS) e [Unicode](unicode.md). Para um DBCS, esses caracteres não padrão são conhecidos como EUDC (caracteres definidos pelo usuário final). O Unicode fornece um recurso semelhante por meio de sua área de uso particular (PUA). Os aplicativos identificam um caractere especificado usando o valor de caractere Unicode ou DBCS associado.

Os valores de caracteres DBCS que podem ser atribuídos dependem do conjunto de caracteres especificado. Cada [página de código](code-pages.md) do Windows do leste asiático tem pelo menos um intervalo de valores reservados para uso como EUDCs. Os intervalos são definidos pela chave do registro [EUDCCodeRange](eudccoderange.md) . Os valores Unicode para essa finalidade sempre vêm do PUA Unicode, os valores U + E000 para U + F8FF, U + F0000 para U + FFFF e U + 100.000 para U + 10FFFD.

Para criar um caractere EUDC ou PUA, o usuário escolhe um valor de caractere que está dentro do intervalo especificado e adiciona o [glifo](uniscribe-glossary.md) à fonte na entrada que corresponde a esse valor de caractere. O usuário cria o glifo usando um editor EUDC ou usando um pacote de fontes adquirido de um fornecedor de fontes. Qualquer fonte DBCS pode conter EUDCs e qualquer fonte Unicode pode conter PUA caracteres. A fonte é chamada de fonte de EUDC/PUA "separada" se ela contiver somente EUDCs. A fonte é uma fonte "" integrada "EUDC/PUA se contiver caracteres padrão, bem como EUDCs.

A fonte EUDC/PUA padrão do sistema é uma fonte que o sistema operacional associa automaticamente a todas as fontes DBCS e Unicode, exceto fontes que têm fontes EUDC/PUA explicitamente associadas. Os aplicativos definem a fonte EUDC/PUA padrão do sistema definindo o valor do nome SystemDefaultEUDCFont na chave do registro [EUDC](eudc.md) . Da mesma forma, os aplicativos podem associar fontes EUDC/PUA separadas com fontes correspondentes, especificando um nome de fonte e um arquivo de fonte associado sob a chave EUDC. O sistema operacional sempre tenta primeiro localizar o EUDC/PUA na fonte atualmente selecionada. Se a fonte não for encontrada, o sistema operacional procurará o caractere na fonte EUDC/PUA associada, se um tiver sido definido para a fonte selecionada no momento. Se ainda não conseguir localizar o caractere, o sistema operacional o procurará na fonte EUDC/PUA padrão do sistema.

As fontes TrueType podem ser instaladas como arquivos. ttf ou como arquivos. TTE. Como o sistema operacional oculta arquivos. TTE, os aplicativos não podem enumerar ou, de outra forma, examinar as fontes instaladas usando funções da API GDI. Em muitos sistemas operacionais, a fonte EUDC/PUA padrão do sistema e as fontes EUDC/PUA separadas são instaladas como arquivos. TTE. Aplicativos como editores EUDC e o painel de controle devem usar entradas de registro para adicionar, modificar e excluir essas fontes.

O uso de caracteres EUDC e PUA não preserva de maneira confiável o significado entre diferentes computadores ou conjuntos de caracteres. Consulte [caracteres de área de uso privado e definido pelo usuário final](end-user-defined-characters.md) para ter mais precauções sobre o uso de caracteres EUDC e pua.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Caracteres da área de uso privado e definido pelo usuário final](end-user-defined-characters.md)
</dt> </dl>

 

 



