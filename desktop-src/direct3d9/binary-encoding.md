---
description: Esta seção detalha a versão binária do formato de arquivo DirectX (.x), conforme introduzido com o lançamento do DirectX 3.0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificação binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f35d4ccd33692cc25c2b99c8c20ed53dc0c7a01a488c738992a9a4f22fbc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460748"
---
# <a name="binary-encoding"></a>Codificação binária

Esta seção detalha a versão binária do formato de arquivo DirectX (.x), conforme introduzido com o lançamento do DirectX 3.0.

O formato binário é uma representação em token do formato de texto. Os tokens podem ser autônomos ou acompanhados por registros de dados primitivos. Tokens autônomos fornecem estrutura gramatical e tokens de influência de registro fornecem os dados necessários.

Observe que todos os dados são armazenados no formato little-endian. Um fluxo de dados binário válido consiste em um header seguido por modelos e/ou objetos de dados.

Esta seção discute os seguintes componentes do formato de arquivo binário e fornece um modelo de exemplo e um objeto de dados binários.

-   [Cabeçalho](header.md)
-   [Tokens](tokens.md)
-   [Registros de token](token-records.md)
-   [Modelos](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [Dados](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [Exemplos](examples.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de formato de arquivo X](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



