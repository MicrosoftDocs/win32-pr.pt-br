---
description: Os aplicativos associam um estágio de mesclagem a cada textura no conjunto de texturas atuais. O Direct3D avalia cada estágio de mesclagem na ordem, começando pela primeira textura no conjunto e terminando com oitavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operações e argumentos de mesclagem de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791662"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Operações e argumentos de mesclagem de textura (Direct3D 9)

Os aplicativos associam um estágio de mesclagem a cada textura no conjunto de texturas atuais. O Direct3D avalia cada estágio de mesclagem na ordem, começando pela primeira textura no conjunto e terminando com oitavo.

O Direct3D aplica as informações de cada textura no conjunto de texturas atuais ao estágio de mesclagem associado a ela. Os aplicativos controlam quais informações de um estágio de textura são usadas chamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api). Você pode definir operações separadas para os canais de cor e alfa, e cada operação usa dois argumentos. Especifique as operações de canal de cores usando o \_ estado de estágio D3DTSS COLOROP; especifique operações alfa usando D3DTSS \_ ALPHAOP. Ambos os Estados de estágio usam valores do tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .

Os argumentos de mesclagem de textura usam os \_ Membros D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 e D3DTSS \_ ALPHARG2 do tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Os valores de argumento correspondentes são identificados usando [D3DTA](d3dta.md).

> [!Note]  
> Você pode desabilitar um estágio de textura e quaisquer estágios de mesclagem de textura subsequentes na cascata, definindo a operação de cor para esse estágio como D3DTOP \_ Disable. Desabilitar a operação de cor efetivamente desabilita a operação alfa também. As operações alfa não podem ser desabilitadas quando as operações de cores estão habilitadas. Definir a operação Alpha como D3DTOP \_ Disable quando a mesclagem de cores está habilitada causa um comportamento indefinido.

 

Para determinar as operações de mesclagem de textura com suporte de um dispositivo, consulte o membro TextureCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> </dl>

 

 
