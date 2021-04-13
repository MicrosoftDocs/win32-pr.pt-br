---
description: Todo desenvolvedor que cria aplicativos em tempo real que usam gráficos 3D está preocupado com a otimização do desempenho. Esta seção fornece diretrizes para obter o melhor desempenho do seu código.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Otimizações de desempenho (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456367"
---
# <a name="performance-optimizations-direct3d-9"></a>Otimizações de desempenho (Direct3D 9)

Todo desenvolvedor que cria aplicativos em tempo real que usam gráficos 3D está preocupado com a otimização do desempenho. Esta seção fornece diretrizes para obter o melhor desempenho do seu código.

-   [Dicas gerais de desempenho](#general-performance-tips)
-   [Bancos de dados e remoção](#databases-and-culling)
-   [Primitivos de envio em lote](#batching-primitives)
-   [Dicas de iluminação](#lighting-tips)
-   [Tamanho da textura](#texture-size)
-   [Transformações de matriz](#matrix-transforms)
-   [Usando texturas dinâmicas](#using-dynamic-textures)
-   [Usando um vértice dinâmico e buffers de índice](#using-dynamic-vertex-and-index-buffers)
-   [Usando malhas](#using-meshes)
-   [Desempenho de buffer Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Dicas gerais de desempenho

-   Desmarque somente quando precisar.
-   Minimize as alterações de estado e agrupe as alterações de estado restantes.
-   Use texturas menores, se puder fazer isso.
-   Desenhe objetos em sua cena de frente para trás.
-   Use as faixas de triângulo em vez de listas e ventiladores. Para obter um desempenho de cache de vértice ideal, organize as faixas para reutilizar vértices de triângulo mais cedo, em vez de mais tarde
-   Degradar normalmente efeitos especiais que exigem um compartilhamento desproporcional de recursos do sistema.
-   Teste constantemente o desempenho do seu aplicativo.
-   Minimize as opções de buffer de vértice.
-   Use buffers de vértice estáticos sempre que possível.
-   Use um buffer de vértice estático grande por FVF para objetos estáticos, em vez de um por objeto.
-   Se seu aplicativo precisar de acesso aleatório no buffer de vértice na memória AGP, escolha um tamanho de formato de vértice que seja múltiplo de 32 bytes. Caso contrário, selecione o menor formato apropriado.
-   Desenhar usando primitivos indexados. Isso pode permitir um cache de vértices mais eficiente no hardware.
-   Se o formato de buffer de profundidade contiver um canal de estêncil, sempre Limpe os canais de profundidade e estêncil ao mesmo tempo.
-   Combine a instrução do sombreador e a saída de dados sempre que possível. Por exemplo:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Bancos de dados e remoção

Criar um banco de dados confiável dos objetos em seu mundo é a chave para um desempenho excelente no Direct3D. É mais importante do que melhorias na rasterização ou no hardware.

Você deve manter a contagem de polígonos mais baixa que possivelmente pode gerenciar. Crie um pequeno número de polígonos criando modelos de baixo polígono desde o início. Adicione polígonos se você puder fazer isso sem sacrificar o desempenho posteriormente no processo de desenvolvimento. Lembre-se de que os polígonos mais rápidos são aqueles que você não desenha.

## <a name="batching-primitives"></a>Primitivos de envio em lote

Para obter o melhor desempenho de renderização durante a execução, tente trabalhar com primitivos em lotes e mantenha o número de alterações de estado de processamento o mais baixo possível. Por exemplo, se você tiver um objeto com duas texturas, agrupe os triângulos que usam a primeira textura e siga-os com o estado de processamento necessário para alterar a textura. Em seguida, agrupe todos os triângulos que usam a segunda textura. O suporte de hardware mais simples para o Direct3D é chamado com lotes de Estados de renderização e lotes de primitivos por meio da HAL (camada de abstração de hardware). Quanto mais efetivamente as instruções forem em lote, menos chamadas de HAL serão executadas durante a execução.

## <a name="lighting-tips"></a>Dicas de iluminação

Como as luzes adicionam um custo por vértice a cada quadro renderizado, você pode melhorar o desempenho de forma significativa com o cuidado de usá-los em seu aplicativo. A maioria das dicas a seguir derivam do máximo, "o código mais rápido é o código que nunca é chamado".

-   Use o menor número possível de fontes leves. Para aumentar o nível de iluminação geral, por exemplo, use a luz ambiente em vez de adicionar uma nova fonte de luz.
-   Luzes direcionais são mais eficientes do que luzes de ponto ou Spotlights. Para luzes direcionais, a direção da luz é fixa e não precisa ser calculada por vértice.
-   Os destaques podem ser mais eficientes do que as luzes de ponto, pois a área fora do cone de luz é calculada rapidamente. Se os Spotlights são mais eficientes ou não depende de quanto de sua cena está acesa pelo destaque.
-   Use o parâmetro Range para limitar as luzes a apenas as partes da cena que você precisa iluminar. Todos os tipos de luz saem bastante cedo quando estão fora do intervalo.
-   Os realces especulares quase duplos são o custo de uma luz. Use-os somente quando precisar. Defina o \_ estado de RENDERIZAÇÃO D3DRS SPECULARENABLE como 0, o valor padrão, sempre que possível. Ao definir materiais, você deve definir o valor de energia especular como zero para desativar os realces especulares para esse material; apenas definir a cor especular como 0, 0, 0 não é suficiente.

## <a name="texture-size"></a>Tamanho da textura

O desempenho de mapeamento de textura depende muito da velocidade da memória. Há várias maneiras de maximizar o desempenho do cache das texturas do seu aplicativo.

-   Mantenha as texturas pequenas. Quanto menores forem as texturas, maior a chance de serem mantidas no cache secundário da CPU principal.
-   Não altere as texturas em uma base por primitiva. Tente manter os polígonos agrupados na ordem das texturas que eles usam.
-   Use texturas quadradas sempre que possível. As texturas cujas dimensões são 256x256 são as mais rápidas. Se seu aplicativo usar quatro texturas 128x128, por exemplo, tente garantir que elas usem a mesma paleta e coloque-as em uma textura 256x256. Essa técnica também reduz a quantidade de permutação de textura. É claro que você não deve usar texturas 256x256, a menos que seu aplicativo exija que muito texturing porque, como mencionado, as texturas devem ser mantidas o menor possível.

## <a name="matrix-transforms"></a>Transformações de matriz

O Direct3D usa as matrizes de mundo e modo de exibição que você definiu para configurar várias estruturas de dados internas. Cada vez que você define um novo mundo ou uma matriz de exibição, o sistema recalcula as estruturas internas associadas. A definição dessas matrizes com frequência – por exemplo, milhares de vezes por quadro – é computacionalmente demorada. Você pode minimizar o número de cálculos necessários concatenando as matrizes de mundo e modo de exibição em uma matriz de exibição de mundo que você define como matriz de mundo, e, em seguida, definindo a matriz de visualização para a identidade. Mantenha cópias em cache das matrizes individuais de mundo e modo de exibição para que você possa modificar, concatenar e restaurar a matriz de mundo conforme necessário. Para maior clareza nesta documentação, os exemplos de Direct3D raramente empregam essa otimização.

## <a name="using-dynamic-textures"></a>Usando texturas dinâmicas

Para descobrir se o driver dá suporte a texturas dinâmicas, verifique o \_ sinalizador D3DCAPS2 DYNAMICTEXTURES da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

Lembre-se das seguintes coisas ao trabalhar com texturas dinâmicas.

-   Eles não podem ser gerenciados. Por exemplo, seu pool não pode ser \_ gerenciado por D3DPOOL.
-   Texturas dinâmicas podem ser bloqueadas, mesmo que elas sejam criadas no \_ padrão D3DPOOL.
-   D3DLOCK \_ descarte é um sinalizador de bloqueio válido para texturas dinâmicas.

É uma boa ideia criar apenas uma textura dinâmica por formato e, possivelmente, por tamanho. Mipmaps dinâmicos, cubos e volumes não são recomendados devido à sobrecarga adicional no bloqueio de cada nível. Para mipmaps, o \_ descarte de D3DLOCK é permitido somente no nível superior. Todos os níveis são descartados bloqueando apenas o nível superior. Esse comportamento é o mesmo para volumes e cubos. Para cubos, o nível superior e a face 0 estão bloqueados.

O pseudocódigo a seguir mostra um exemplo de como usar uma textura dinâmica.


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>Usando um vértice dinâmico e buffers de índice

Bloquear um buffer de vértices estáticos enquanto o processador de gráficos está usando o buffer pode ter uma penalidade de desempenho significativa. A chamada de bloqueio deve aguardar até que o processador de gráficos termine de ler os dados de vértice ou de índice do buffer antes que ele possa retornar ao aplicativo de chamada, um atraso significativo. O bloqueio e a renderização de um buffer estático várias vezes por quadro também impede que o processador de gráficos faça o armazenamento em buffer de comandos de renderização, já que ele deve concluir os comandos antes de retornar o ponteiro de bloqueio. Sem comandos em buffer, o processador de gráficos permanece ocioso até que o aplicativo termine de preencher o buffer de vértices ou o buffer de índice e emita um comando de renderização.

O ideal é que os dados de vértice ou de índice nunca mudem, mas isso nem sempre é possível. Há muitas situações em que o aplicativo precisa alterar os dados do vértice ou do índice a cada quadro, talvez até várias vezes por quadro. Para essas situações, o vértice ou buffer de índice deve ser criado com D3DUSAGE \_ Dynamic. Esse sinalizador de uso faz com que o Direct3D Otimize para operações de bloqueio frequentes. D3DUSAGE \_ Dynamic só é útil quando o buffer é bloqueado com frequência; os dados que permanecem constantes devem ser colocados em um buffer estático de índice ou de vértice.

Para receber uma melhoria de desempenho ao usar buffers de vértice dinâmicos, o aplicativo deve chamar [**IDirect3DVertexBuffer9:: Lock**](/windows/desktop/api) ou [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) com os sinalizadores apropriados. D3DLOCK \_ descarte indica que o aplicativo não precisa manter o vértice antigo ou os dados de índice no buffer. Se o processador de gráficos ainda estiver usando o buffer quando o bloqueio for chamado com descarte de D3DLOCK \_ , um ponteiro para uma nova região de memória será retornado em vez dos dados de buffer antigos. Isso permite que o processador de gráficos continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer. Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando o processador de gráficos é concluído com ele. Observe que o bloqueio de um buffer com descarte de D3DLOCK \_ sempre descarta todo o buffer, especificando que um campo de tamanho de deslocamento diferente de zero ou limite não preserva as informações em áreas desbloqueadas do buffer.

Há casos em que a quantidade de dados que o aplicativo precisa armazenar por bloqueio é pequena, como adicionar quatro vértices para renderizar um Sprite. D3DLOCK \_ NoOverwrite indica que o aplicativo não substituirá os dados que já estão em uso no buffer dinâmico. A chamada de bloqueio retornará um ponteiro para os dados antigos, permitindo que o aplicativo Adicione novos dados em regiões não utilizadas do vértice ou buffer de índice. O aplicativo não deve modificar vértices ou índices usados em uma operação de desenho, pois eles ainda podem estar em uso pelo processador de gráficos. O aplicativo deve usar o \_ descarte D3DLOCK depois que o buffer dinâmico estiver cheio para receber uma nova região de memória, descartando os dados antigos do vértice ou do índice depois que o processador de gráficos for concluído.

O mecanismo de consulta assíncrona é útil para determinar se os vértices ainda estão em uso pelo processador de gráficos. Emita uma consulta do tipo \_ evento D3DQUERYTYPE após a última chamada de DrawPrimitive que usa os vértices. Os vértices não estão mais em uso quando [**IDirect3DQuery9:: GetData**](/windows/desktop/api) retorna S \_ OK. Bloquear um buffer com \_ descartar D3DLOCK ou nenhum sinalizador sempre garantirá que os vértices sejam sincronizados corretamente com o processador de gráficos. no entanto, o uso do bloqueio sem sinalizadores incorrerá na penalidade de desempenho descrita anteriormente. Outras chamadas à API, como [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api), [**IDirect3DDevice9:: EndScene**](/windows/desktop/api)e [**IDirect3DDevice9::P reenviadas**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) não garantem que o processador de gráficos termine de usar vértices.

Veja abaixo as maneiras de usar buffers dinâmicos e os sinalizadores de bloqueio apropriados.


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>Usando malhas

Você pode otimizar as malhas usando triângulos indexados do Direct3D em vez de faixas de triângulo indexadas. O hardware descobrirá que 95% dos triângulos sucessivos realmente formam as faixas e se ajustam de acordo. Muitos drivers também fazem isso para hardware mais antigo.

Os objetos de malha D3DX podem ter cada triângulo, ou face, marcado com um DWORD, chamado de atributo dessa face. A semântica do DWORD é definida pelo usuário. Eles são usados pelo D3DX para classificar a malha em subconjuntos. O aplicativo define os atributos por face usando a chamada [**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) . O método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) tem uma opção para agrupar os vértices de malha e rostos em atributos usando a \_ opção ATTRSORT de D3DXMESHOPT. Quando isso é feito, o objeto de malha calcula uma tabela de atributos que pode ser obtida pelo aplicativo chamando [**ID3DXBaseMesh:: Getattributetable**](id3dxbasemesh--getattributetable.md). Essa chamada retornará 0 se a malha não estiver classificada por atributos. Não há como um aplicativo definir uma tabela de atributos porque ele é gerado pelo método **ID3DXMesh:: Optimize** . A classificação de atributo é sensível a dados, portanto, se o aplicativo souber que uma malha é um atributo classificado, ele ainda precisará chamar **ID3DXMesh:: Optimize** para gerar a tabela de atributos.

Os tópicos a seguir descrevem os diferentes atributos de uma malha.

### <a name="attribute-id"></a>ID do atributo

Uma ID de atributo é um valor que associa um grupo de rostos a um grupo de atributos. Essa ID descreve qual subconjunto de rostos [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) deve desenhar. As IDs de atributo são especificadas para as faces no buffer de atributo. Os valores reais das IDs de atributo podem ser qualquer coisa que caiba em 32 bits, mas é comum usar 0 a n, em que n é o número de atributos.

### <a name="attribute-buffer"></a>Buffer de atributo

O buffer de atributo é uma matriz de DWORDs (um por face) que especifica a qual grupo de atributos cada face pertence. Esse buffer é inicializado para zero na criação de uma malha, mas é preenchido pelas rotinas de carga ou deve ser preenchido pelo usuário se mais de um atributo com ID 0 for desejado. Esse buffer contém as informações que são usadas para classificar a malha com base em atributos em [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md). Se nenhuma tabela de atributos estiver presente, [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) examinará esse buffer para selecionar as faces do atributo fornecido a serem desenhados.

### <a name="attribute-table"></a>Tabela de atributos

A tabela de atributos é uma estrutura de propriedade e mantida pela malha. A única maneira de gerar um a ser gerado é chamando [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) com classificação de atributo ou otimização mais forte habilitada. A tabela de atributos é usada para iniciar rapidamente uma única chamada primitiva de desenho para [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md). O único outro uso é que o progresso das malhas também mantém essa estrutura, portanto, é possível ver quais faces e vértices estão ativos no nível de detalhes atual.

## <a name="z-buffer-performance"></a>Desempenho de buffer Z

Os aplicativos podem aumentar o desempenho ao usar o buffer z e texturização, garantindo que as cenas sejam renderizadas da frente para trás. Buffers z texturizados primitivos são pré-testados em relação ao buffer z em uma base de linha de varredura. Se uma linha de varredura for ocultada por um polígono renderizado anteriormente, o sistema a rejeita com rapidez e eficiência. O buffer Z pode melhorar o desempenho, mas a técnica é mais útil quando uma cena desenha os mesmos pixels mais de uma vez. Isso é difícil de calcular exatamente, mas geralmente, você pode obter uma boa aproximação. Se os mesmos pixels forem desenhados menos de duas vezes, você pode obter o melhor desempenho desativando o buffer z e renderizando a cena de trás para frente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
