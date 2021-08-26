---
title: Convertendo tevdef
description: O exemplo de código a seguir é uma definição de ambiente de textura do íris GL que especifica o parâmetro de ambiente de textura de decal de TV \_
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
- Portabilidade do íris GL, tevdef
- portando do íris GL, tevdef
- portando para OpenGL do íris GL, tevdef
- Portabilidade OpenGL do íris GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7feef33c2aa725c6e5bb91782fe43fdc6a84d23db8aa412f02c07b6ec588f719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887876"
---
# <a name="translating-tevdef"></a>Convertendo tevdef

O exemplo de código a seguir é uma definição de ambiente de textura do íris GL que especifica o parâmetro de ambiente de textura de decal de TV \_ :


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



e o mesmo código traduzido para OpenGL:


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



A tabela a seguir lista os parâmetros de ambiente de textura do íris GL e seus parâmetros OpenGL equivalentes.



| Parâmetro do íris GL     | Parâmetro OpenGL             |
|-----------------------|------------------------------|
| \_modular de TV          | GL \_ modular                 |
| DECAL de TV \_             | \_Decal GL                    |
| TV \_ Blend             | a \_ combinação GL                    |
| cor da TV \_             | cor do GL \_ Texture \_ env \_      |
| Alfa da TV \_             | Nenhum equivalente OpenGL direto. |
| \_seleção de componente de TV \_ | Nenhum equivalente OpenGL direto. |



 

Para obter mais informações sobre os parâmetros de ambiente de textura, consulte [**glTexEnv**](gltexenv-functions.md).

 

 




