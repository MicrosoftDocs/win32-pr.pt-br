---
description: 'Constantes de argumento de textura são usadas como valores para os seguintes membros do tipo enumerado D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db520bee7e4352b3242824819cc579acd82b1d013d290b2155d54170bc478c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527310"
---
# <a name="d3dta"></a>D3DTA

Constantes de argumento de textura são usadas como valores para os seguintes membros do tipo enumerado [**D3DTEXTURESTAGESTATETYPE:**](./d3dtexturestagestatetype.md)

-   ALFAARG0 D3DTSS \_
-   D3DTSS \_ ALPHAARG1
-   ALFAARG2 D3DTSS \_
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

De definir e recuperar argumentos de textura chamando os [**métodos SetTextureStageState**](/windows/desktop/api) e [**GetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)

Sinalizadores de argumento

Você pode combinar um sinalizador de argumento com um modificador, mas dois sinalizadores de argumento não podem ser combinados.



| \#Definir          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONSTANTE D3DTA \_   | Selecione uma constante em um estágio de textura. O valor padrão é 0xffffffff.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ ATUAL    | O argumento de textura é o resultado do estágio de mesclagem anterior. No primeiro estágio de textura (estágio 0), esse argumento é equivalente a D3DTA \_ DIFUSO. Se o estágio de mesclagem anterior usar uma textura de mapa de elevação (a operação D3DTOP BUMPENVMAP), o sistema escolherá a textura do estágio antes da textura do mapa de \_ elevação. Se s representar o estágio de textura atual e s - 1 contiver uma textura de mapa de aumento, esse argumento se tornará a saída de resultado pelo estágio de textura s - 2. As permissões são leitura/gravação. |
| D3DTA \_ DIFUSO    | O argumento de textura é a cor difusa interpolada de componentes de vértice durante o sombreamento do Gouraud. Se o vértice não contém uma cor difusa, a cor padrão é 0xffffffff. As permissões são somente leitura.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Valor de máscara para todos os argumentos; não usado ao definir argumentos de textura.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ SPECULAR   | O argumento de textura é a cor especular interpolada de componentes de vértice durante o sombreamento do Gouraud. Se o vértice não contém uma cor especular, a cor padrão é 0xffffffff. As permissões são somente leitura.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ TEMP       | O argumento de textura é uma cor de registro temporária para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ [ \_ TSSARGTEMP D3DPMISCCAPS](d3dpmisccaps.md) estiver presente. O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0). As permissões são leitura/gravação.                                                                                                                                                                                                                                   |
| TEXTURA D3DTA \_    | O argumento de textura é a cor da textura para esse estágio de textura. As permissões são somente leitura.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | O argumento de textura é o fator de textura definido em uma chamada anterior para [**SetRenderState**](/windows/desktop/api) com o valor de estado de renderização [**\_ TEXTUREFACTOR D3DRS.**](./d3drenderstatetype.md) As permissões são somente leitura.                                                                                                                                                                                                                                                       |



 

Sinalizadores modificador

Um sinalizador de argumento pode ser combinado com um dos seguintes sinalizadores modificador.



| \#Definir              | Description                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | Replique as informações alfa para todos os canais de cores antes que a operação seja concluída. Este é um modificador de leitura. |
| COMPLEMENTO D3DTA \_     | Tome o complemento do argumento x, (1.0 - x). Este é um modificador de leitura.                                     |



 

## <a name="constant-information"></a>Informações constantes



|   Requisito                       |  Valor           |
|--------------------------|-------------|
| parâmetro                   | d3d9types.h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
