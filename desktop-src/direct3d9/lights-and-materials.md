---
description: As luzes são usadas para iluminar objetos em uma cena.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Luzes e materiais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5ace2a80bb79d192fadc5376256eedf9229be9a36fa1d200341ccf28e961fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277516"
---
# <a name="lights-and-materials-direct3d-9"></a>Luzes e materiais (Direct3D 9)

As luzes são usadas para iluminar objetos em uma cena. Quando a iluminação está habilitada, o Direct3D calcula a cor de cada vértice do objeto com base em uma combinação de:

> [!Note]  
> Esta seção é apenas para o pipeline de função fixa. Os sombreadores programáveis executam toda a iluminação de modo explícito.

 

-   A cor do material atual e o texels em um mapa de textura associado.
-   As cores difusas e especulares do vértice, se especificado.
-   A cor e a intensidade da luz produzida por fontes de iluminação de cena ou o nível de luz ambiente da cena.

Ao usar a iluminação e os materiais do Direct3D, você permite que o Direct3D manipule os detalhes de iluminação para você. Os usuários avançados podem executar a iluminação por conta própria, se desejado.

A forma como você trabalha com a iluminação e os materiais faz uma grande diferença na aparência da cena renderizada. Os materiais definem como a luz é refletida por uma superfície. Níveis de luz direta e ambiente definem a luz refletida. Você deve usar materiais para renderizar uma cena se a iluminação estiver habilitada. As luzes não são necessárias para renderizar uma cena, mas os detalhes em uma cena renderizada sem luz não estão visíveis. Na melhor das hipóteses, a renderização de uma cena apagada resulta em uma silhueta dos objetos nela. Isso não fornece detalhes suficientes para a maioria das finalidades.

## <a name="direct-light-vs-ambient-light"></a>Luz direta versus luz ambiente

Embora as luzes direta e ambiente iluminem objetos em uma cena, elas são independentes uma da outra, têm efeitos muito diferentes e exigem que você trabalhe com elas de formas completamente diferentes.

A luz direta é apenas: direta. A luz direta sempre tem direção e cor, além de ser um fator para algoritmos de sombreamento, como sombreamento de Gouraud. Diferentes tipos de luzes emitem luz direta de formas diferentes, o que cria efeitos especiais de atenuação. Você cria um conjunto de parâmetros leves para luz direta chamando o método [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) .

Luz ambiente está efetivamente em qualquer lugar em uma cena. Você pode considerar isso como um nível geral de luz que preenche uma cena inteira, independentemente dos objetos e de suas localizações nessa cena. A luz ambiente não tem posição ou direção, somente cor e intensidade. Cada luz adiciona detalhes à luz ambiente geral em uma cena. Defina o nível de luz ambiente com uma chamada para o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) , especificando o \_ ambiente D3DRS como o parâmetro de *estado* e a cor RGBA desejada como o parâmetro de valor.

A cor de luz ambiente assume a forma de um valor RGBA, onde cada componente é um valor inteiro de 0 a 255. Isso é diferente da maioria dos valores de cores no Direct3D.

Você pode usar a macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para gerar valores RGBA. Os componentes vermelhos, verdes e azuis são combinados para formar a cor final da luz ambiente. O componente alfa controla a transparência da cor. Ao usar a aceleração de hardware ou a emulação de RGB, o componente alfa é ignorado.

## <a name="direct3d-light-model-vs-nature"></a>Modelo Direct3D Light versus natureza

Na natureza, quando a luz é emitida de uma fonte, ela é refletido por centenas, se não milhares ou milhões de objetos antes de chegar aos olhos do usuário. Cada vez que ele é refletido, uma luz é absorvida por uma superfície, algumas estão espalhados em direções aleatórias e o restante prossegue para outra superfície ou a atenção do usuário. Esse processo continua até que a luz seja reduzida a nada ou um usuário perceba a luz.

Obviamente, os cálculos necessários para simular perfeitamente o comportamento natural de luz são muito demorados para uso em elementos gráficos de tempo real do Direct3D. Portanto, pensando na velocidade, o modelo de luz do Direct3D se aproxima da maneira como a luz funciona no mundo natural. O Direct3D descreve a luz em termos de componentes de vermelhos, verdes e azuis que são combinados para criar uma cor final.

No Direct3D, quando a luz é refletida por uma superfície, a cor da luz interage matematicamente com a superfície para criar a cor eventualmente exibida na tela. Para obter informações específicas sobre os algoritmos usados pelo Direct3D, consulte [matemática de iluminação (Direct3D 9)](mathematics-of-lighting.md).

O modelo de luz do Direct3D generaliza a luz em dois tipos: luzes ambiente e direta. Cada uma tem atributos diferentes e interage com o material de uma superfície de maneiras diferentes. A luz ambiente é muito espalhada, portanto, sua direção e fonte são indeterminadas: ela mantém um nível baixo de intensidade em todos os lugares. A iluminação indireta usada por fotógrafos é um bom exemplo de luz ambiente. Assim como na natureza, a luz ambiente no Direct3D não tem direção real ou fonte, apenas uma cor e uma intensidade. Na verdade, o nível de luz ambiente é independente de qualquer objeto em uma cena que gera luz. A luz ambiente não contribui para a reflexão especular.

A luz direta é gerada por uma fonte em uma cena; sempre tem cor e a intensidade, além de se deslocar em uma direção especificada. A luz direta interage com o material de uma superfície para criar realces especulares e sua direção é usada como um fator em algoritmos de sombreamento, incluindo sombreamento de Gouraud. Quando a luz direta é refletida, ela não contribui para o nível de luz ambiente em uma cena. As fontes em uma cena que geram luz direta têm características diferentes que afetam como iluminam uma cena.

Além disso, o material do polígono tem propriedades que afetam como ele reflete a luz recebida. Você define uma única característica de reflexão que descreve como o material reflete a luz ambiente, além de definir características individuais para determinar a reflexão especulares e difusa do material. Para obter mais informações, consulte [materiais (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Valores de cor para luzes e materiais

O Direct3D descreve a cor em termos de quatro componentes – vermelho, verde, azul e alfa-que se combinam para fazer uma cor final. A estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) C++ é definida para conter valores para cada componente. Cada membro é um valor de ponto flutuante que normalmente varia de 0,0 a 1,0, inclusive. Embora as luzes e os materiais usem a mesma estrutura para descrever a cor, os valores na estrutura são usados um pouco diferente de cada um.

Os valores de cor para fontes de iluminação representam a quantidade de um componente de luz específico emitido. Como as luzes não usam um componente alfa, apenas os componentes de vermelhos, verdes e azuis da cor são relevantes. Você pode visualizar os três componentes como lentes vermelhas, verdes e azuis em uma televisão de projeção. Cada lente pode estar deslocada (por um valor de 0,0 no membro apropriado), poderá ser o mais brilhante possível (um valor de 1,0) ou pode estão em algum nível no meio. As cores das lentes são combinadas para criar a cor da luz final. Uma combinação como R(1,0), G(1,0), B(1,0) cria uma luz branca, onde R(0,0) G(0,0), B(0,0), não emite luz. Você pode fazer uma luz que emite um único componente, resultando em uma luz de vermelha, verde ou azul pura; ou, a luz pode usar combinações para emitir cores como amarelo ou roxo. Você pode até mesmo definir valores de componentes negativos para criar uma "luz escura" que remove a luz de uma cena. Ou, você pode definir os componentes com algum valor maior do que 1,0 para criar uma luz muito clara.

Por outro lado, com os materiais, os valores de cor representam o quanto um componente de luz é refletido por uma superfície renderizada com esse material. Um material cujos componentes de cor são R(1,0), G(1,0), B(1,0), A(1,0) reflete a luz recebida. Da mesma forma, um material com R(0,0), G(1,0), B(0,0), A(1,0) reflete toda a luz verde direcionada a ele. Os materiais têm diversos valores de reflexão para criar vários tipos de efeitos.

Informações adicionais estão contidas em: [tipos de luz (Direct3D 9)](light-types.md)e [Propriedades de luz (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 
