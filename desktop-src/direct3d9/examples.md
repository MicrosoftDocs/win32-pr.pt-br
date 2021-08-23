---
description: Seguem dois exemplos de definições de modelo binário e um exemplo de objeto de dados binários.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Exemplos (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8b8e2a9c500042e9b8d7c7fd911ab74b2f428d1ef814aca9e5fda1be7dcab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523093"
---
# <a name="examples-direct3d-9-graphics"></a>Exemplos (gráficos do Direct3D 9)

Seguem dois exemplos de definições de modelo binário e um exemplo de objeto de dados binários.

> [!Note]  
> Os dados são armazenados no formato little-endian, que não é mostrado nesses exemplos.

 

O modelo fechado RGB é identificado pelo UUID {55b6d780-37ec-11D0-AB39-0020af71e433} e tem três membros-r, g e b-cada do tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



O modelo fechado Matrix4x4 é identificado pelo UUID {55b6d781-37ec-11D0-AB39-0020af71e433} e tem um membro-uma matriz bidimensional chamada Matrix-do tipo float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



O objeto de dados binários a seguir mostra uma instância do modelo RGB definido anteriormente. O objeto de exemplo é denominado Blue e seus três membros-r, g e b-têm os valores 0,0, 0,0 e 1,0, respectivamente.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação binária](binary-encoding.md)
</dt> </dl>

 

 



