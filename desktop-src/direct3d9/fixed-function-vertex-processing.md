---
description: No pipeline de vértice de função fixa, o processamento dos vértices em um buffer de vértice aplica as matrizes de transformação atuais para o dispositivo.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Processamento de vértice de função fixa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827a293a4fbd552327d93076de773aec90dbd895faf3c086f4794036978984fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988016"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Processamento de vértice de função fixa (Direct3D 9)

No pipeline de vértice de função fixa, o processamento dos vértices em um buffer de vértice aplica as matrizes de transformação atuais para o dispositivo. Operações de vértice como iluminação, geração de sinalizadores de clipes e extensões de atualização também podem ser aplicadas, opcionalmente. Ao usar o processamento de vértice de função fixa, modificar os elementos no buffer de vértice de destino é controlado pelo sinalizador [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) . Esse sinalizador se aplica somente ao processamento de vértice de função fixa. A interface [**IDirect3DDevice9**](/windows/desktop/api) expõe o método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) para processar vértices. Você processa vértices de um sombreador de vértice para o conjunto de fluxos de dados de entrada, gerando um único fluxo de dados de vértice intercalados para o buffer de vértice de destino chamando o método **IDirect3DDevice9::P rocessvertices** . O método aceita cinco parâmetros que descrevem o local e a quantidade de vértices que o método se destina, o buffer de vértice de destino e as opções de processamento. Após a chamada, o buffer de destino contém os dados de vértice processados.

O primeiro, o segundo e o terceiro parâmetros, SrcStartIndex, DestIndex e Contagemdevértice, refletem o índice do primeiro vértice a ser carregado, o índice dentro do buffer de destino no qual os vértices serão colocados e o número total de vértices para processar e colocar no buffer de destino, respectivamente. O quarto parâmetro, pDestBuffer, deve ser definido como o endereço da interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) do objeto de buffer de vértice que receberá os vértices de origem. O parâmetro SrcStartIndex Especifica o índice no qual o método deve iniciar o processamento de vértices.

O parâmetro final, flags, determina as opções de processamento especial para o método. Você pode definir esse parâmetro como 0 para o processamento de vértice padrão ou para [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) para otimizar o processamento em algumas situações. Você também pode combinar o \_ valor de DONOTCOPYDATA D3DPV com um ou mais valores de [D3DLOCK](d3dlock.md) apropriados para o buffer de destino. Quando você define sinalizadores como 0, os componentes de vértice do formato de vértice do buffer de vértices de destino que não são afetados pela operação de vértice ainda são copiados do sombreador de vértice ou definidos como 0. No entanto, ao usar D3DPV \_ DONOTCOPYDATA, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) não substitui as informações de coordenadas de cor e de textura no buffer de destino, a menos que esses dados sejam gerados pelo Direct3D. A cor difusa é gerada quando a iluminação está habilitada, ou seja, \_ a iluminação D3DRS é definida como **true**. A cor especular é gerada quando a iluminação está habilitada e o especular está habilitado, ou seja, D3DRS \_ SPECULARENABLE e D3DRS \_ Lighting são definidos como **true**. A cor especular também é gerada quando a neblina está habilitada. As coordenadas de textura são geradas quando a transformação de textura ou a geração de textura está habilitada. **IDirect3DDevice9::P rocessvertices** usa os Estados de renderização atuais para determinar qual processamento de vértice deve ser feito.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Configurações de uso FVF para buffers de vértice de destino

O método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requer configurações específicas para o [D3DFVF](d3dfvf.md) do buffer de vértice de destino. As configurações de uso de FVF devem ser compatíveis com as configurações atuais para processamento de vértice.

Para o processamento de vértice de função fixa, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) requer as seguintes configurações de FVF:

-   O tipo de posição é sempre [D3DFVF \_ XYZRHW](d3dfvf.md) ; portanto, D3DFVF \_ XYZ e D3DFVF \_ XYZB1 por meio de D3DFVF \_ XYZB5 são inválidos.
-   Os sinalizadores [D3DFVF \_ normal](d3dfvf.md), D3DFVF \_ RESERVED0 e D3DFVF \_ RESERVED2 não devem ser definidos.
-   O [sinalizador \_ difuso D3DFVF](d3dfvf.md) deve ser definido se uma operação OR das seguintes condições retornar true:
    -   A iluminação está habilitada; ou seja, a \_ iluminação D3DRS é **verdadeira**.
    -   A iluminação está desabilitada, a cor difusa está presente nos fluxos de vértice de entrada e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) não está definido.
-   O [sinalizador \_ especular D3DFVF](d3dfvf.md) deve ser definido se uma operação OR das seguintes condições retornar true:
    -   A iluminação está habilitada e a cor especular está habilitada; ou seja, D3DRS \_ SPECULARENABLE é **true**.
    -   A iluminação está desabilitada, a cor especular está presente nos fluxos de vértice de entrada e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) não está definido.
    -   A neblina de vértice está habilitada; ou seja, D3DRS \_ FOGVERTEXMODE não está definido como D3DFOG \_ None.

Além disso, a contagem de coordenadas de textura deve ser definida da seguinte maneira:

-   Se a transformação de textura e a geração de textura estiverem desabilitadas para todos os estágios de textura ativos e o [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) não estiver definido, o número e o tipo de coordenadas de textura de saída serão necessários para corresponder às coordenadas de textura de vértice de entrada. Se D3DPV \_ DONOTCOPYDATA for definido e a transformação de textura e a geração de textura estiverem desabilitadas, as coordenadas de textura de saída serão ignoradas.
-   Se a transformação de textura ou a geração de textura estiver habilitada para qualquer estágio de textura ativa, o vértice de saída poderá precisar conter mais conjuntos de coordenadas de textura do que o vértice de entrada. Isso ocorre devido à proliferação de coordenadas de textura daquelas que estão sendo geradas pela geração de textura ou derivadas por transformações de textura. Observe que uma proliferação semelhante de coordenadas de textura ocorre durante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) chamadas, mas não é visível para o programador de aplicativos. Nesse caso, o Direct3D gera um novo conjunto de coordenadas de textura. O novo conjunto de coordenadas de textura é derivado percorrendo os estágios de textura e analisando as configurações de geração de textura, transformação de textura e índice de coordenadas de textura para determinar se um conjunto exclusivo de coordenadas de textura é necessário para esse estágio. Cada vez que um novo conjunto é necessário, ele é alocado em ordem crescente. Observe que o requisito máximo e típico é um conjunto por etapa, embora possa ser menos devido ao compartilhamento de coordenadas de textura não transferidas por meio de D3DTSS \_ TEXCOORDINDEX.

Portanto, para cada estágio de textura, um novo conjunto de coordenadas de textura será gerado se uma textura estiver associada a esse estágio e qualquer uma das seguintes condições for verdadeira:

-   A geração de textura está habilitada para esse estágio.
-   A transformação de textura está habilitada para esse estágio.
-   Coordenadas de textura de entrada não transtransformadas são referenciadas por meio de D3DTSS \_ TEXCOORDINDEX pela primeira vez.

Quando o Direct3D está gerando coordenadas de textura, o aplicativo é necessário para executar as seguintes ações:

1.  Use um buffer de vértice de destino com o uso FVF apropriado.
2.  Reprogramare o D3DTSS \_ TEXCOORDINDEX do estágio de textura de acordo com o posicionamento das coordenadas de textura em processo. Observe que a reprogramação da configuração D3DTSS \_ TEXCOORDINDEX ocorre quando o buffer de vértice processado é usado em [**IDirect3DDevice9 subsequente::D Rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e [**IDirect3DDevice9::D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) chamadas de rawindexedprimitive.

Por fim, a dimensionalização da coordenada de textura ([D3DFVF \_ TEX0](d3dfvf.md) até D3DFVF \_ TEX8) deve ser definida da seguinte maneira:

-   Para cada conjunto de coordenadas de textura, se a transformação de textura e a geração de textura estiverem desabilitadas, a dimensionalidade da coordenada de textura de saída deverá corresponder à entrada. Se a transformação de textura estiver habilitada, a dimensionalidade de saída deverá corresponder à contagem definida pelas \_ configurações D3DTTFF COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3 ou D3DTTFF \_ COUNT4. Se a transformação de textura estiver desabilitada e a geração de textura estiver habilitada, a dimensionalidade de saída deverá corresponder às configurações do modo de geração de textura; Atualmente, todos os modos geram três valores float.

Quando [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) falha devido a um código de FVF de buffer de vértice de destino incompatível, o código esperado é impresso para a saída de depuração (somente compilações de depuração).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
