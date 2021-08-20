---
description: Crie links simbólicos que usam um caminho absoluto ou relativo usando a função CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Criando links simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0340dc362ff550ab2d74e533ac66e74622c965266440103d6f6ec155bfa80f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150852"
---
# <a name="creating-symbolic-links"></a>Criando links simbólicos

A função [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) permite que você crie links simbólicos usando um caminho absoluto ou relativo.

Links simbólicos podem ser links absolutos ou relativos. Links absolutos são links que especificam cada parte do nome do caminho; os links relativos são determinados em relação ao local em que os especificadores de link estão em um caminho especificado. Os links relativos são especificados usando as seguintes convenções:

-   Ponto (. e..) convenções — por exemplo, ".. \\ " resolve o caminho relativo ao diretório pai.
-   Nomes sem barras ( \\ ) — por exemplo, "tmp" resolve o caminho relativo ao diretório atual.
-   relativa à raiz — por exemplo, " \\ Windows \\ System32" resolve para a "*unidade atual*: \\ Windows \\ System32". directory
-   diretório de trabalho atual – relativo — por exemplo, se o diretório de trabalho atual for "c: \\ Windows \\ system32", "C:File.txt" será resolvido para "C: \\ Windows \\ system32 \\File.txt".

    **Observação**  Se você especificar um link relativo do diretório de trabalho atual, ele será criado como um link absoluto, devido à maneira como o diretório de trabalho atual é processado com base no usuário e no thread.

Um link simbólico também pode conter pontos de junção e pastas montadas como parte do nome do caminho.

Links simbólicos podem apontar diretamente para um arquivo ou diretório remoto usando o caminho UNC.

Links simbólicos relativos são restritos a um único volume.

## <a name="example-of-an-absolute-symbolic-link"></a>Exemplo de um link simbólico absoluto

Neste exemplo, o caminho original contém um componente, '*x*', que é um link simbólico absoluto. Quando '*x*' é encontrado, o fragmento do caminho original até e incluindo '*x*' é completamente substituído pelo caminho que é apontado por '*x*'. O restante do caminho depois de '*x*' é anexado a esse novo caminho. Esse agora se torna o caminho modificado.

X: "C: \\ Alpha \\ beta \\ absLink \\ \\ arquivo gama"

Link: "absLink" é mapeado para " \\ \\ machineB \\ share"

Caminho modificado: " \\ \\ machineB \\ compartilhar \\ \\ arquivo gama"

## <a name="example-of-a-relative-symbolic-links"></a>Exemplo de links simbólicos relativos

Neste exemplo, o caminho original contém um componente '*x*', que é um link simbólico relativo. Quando '*x*' for encontrado, '*x*' será completamente substituído pelo novo fragmento apontado por '*x*'. O restante do caminho após '*x*' é anexado ao novo caminho. Todos os pontos (..) neste novo caminho substituem os componentes que aparecem antes dos pontos (..). Cada conjunto de pontos substitui o componente anterior. Se o número de pontos (..) exceder o número de componentes, um erro será retornado. Caso contrário, quando toda a substituição de componentes for concluída, o caminho final e modificado permanecerá.

X: C: \\ Alpha \\ beta \\ link \\ de \\ arquivo gama

Link: "link" é mapeado para ".. \\ .. \\ teta

Caminho modificado: "C: \\ Alpha \\ beta \\ .. \\ .. \\ \\arquivo gama de teta \\ "

Caminho final: "C: \\ teta \\ gama \\ File"

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Links simbólicos](symbolic-links.md)
</dt> <dt>

[Links físicos e junções](hard-links-and-junctions.md)
</dt> <dt>

[Nomeando arquivos, caminhos e namespaces](naming-a-file.md)
</dt> </dl>

 

 



