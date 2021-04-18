---
description: Esta seção detalha a versão binária do formato de arquivo DirectX (. x), conforme introduzido com o lançamento do DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificação binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814390"
---
# <a name="binary-encoding"></a>Codificação binária

Esta seção detalha a versão binária do formato de arquivo DirectX (. x), conforme introduzido com o lançamento do DirectX 3,0.

O formato binário é uma representação indexada do formato de texto. Os tokens podem ser autônomos ou acompanhados por registros de dados primitivos. Tokens autônomos fornecem estrutura gramatical e tokens de registro fornecem os dados necessários.

Observe que todos os dados são armazenados no formato little-endian. Um fluxo de dados binários válido consiste em um cabeçalho seguido por modelos e/ou objetos de dados.

Esta seção aborda os seguintes componentes do formato de arquivo binário e fornece um modelo de exemplo e um objeto de dados binários.

-   [Cabeçalho](header.md)
-   [Token](tokens.md)
-   [Registros de token](token-records.md)
-   [Modelos](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [Dados](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [Exemplos](examples.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[X referência de formato de arquivo](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



