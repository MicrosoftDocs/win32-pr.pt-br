---
description: As texturas tradicionais são consideradas texturas de elemento único.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Texturas de vários elementos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a434d1e6c6a892c794551aa0caf34890f3def9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813246"
---
# <a name="multiple-element-textures-direct3d-9"></a>Texturas de vários elementos (Direct3D 9)

As texturas tradicionais são consideradas texturas de elemento único. Texturas com vários elementos permitem que os aplicativos gravem simultaneamente em vários elementos de uma textura a partir do sombreador de pixel. O resultado na próxima passagem de renderização é que um aplicativo pode usar um ou mais elementos como uma textura de elemento único, ou seja, como entradas para o sombreador de pixel. Esses elementos adicionais podem ser considerados como um armazenamento temporário para resultados intermediários que serão usados em uma passagem posterior pelo aplicativo.

A primeira geração de hardware que expõe esse recurso tem as seguintes restrições:

-   Todas as superfícies de textura de vários elementos serão alocadas automaticamente. Essa limitação é abordada tratando isso como um novo tipo de formato de superfície com vários canais RGBA intercalados.
-   Todos os elementos da textura de vários elementos podem ter a mesma profundidade de bits. Essa limitação é expressa pelo nome dos novos formatos de superfície.
-   Uma textura de vários elementos não pode ser primária/exibível. Em outras palavras, ela deve ser apenas fora da tela. Essa limitação é expressa pela enumeração de formato de superfície.
-   Não é permitido o pontilhamento, o teste alfa, o fogging, a mesclagem, a operação ou o mascaramento. Nenhum processamento de sombreador após o pixel é feito, exceto o teste z-Test e stencil.
-   A textura não pode ser uma mipmap. A criação da cadeia MIP falhará.
-   O mesmo elemento não pode ser definido como uma textura ao mesmo tempo em que é um destino de renderização. No entanto, elementos diferentes da mesma superfície de textura de vários elementos podem ser simultaneamente texturas e processar destinos.
-   Não há suporte para anti-aliasing.
-   As superfícies de textura de vários elementos, quando usadas como uma textura, não podem ser filtradas. Essa limitação pode ser verificada usando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   As superfícies de textura de vários elementos não podem ser bloqueadas.
-   Mais de uma superfície de textura de vários elementos pode ser usada simultaneamente atribuindo cada uma a várias fases, assim como acontece com texturas normais.
-   As superfícies de textura de vários elementos dão suporte à conversão de gama de 2,2 a 1,0 para a conversão em uma operação de leitura, assim como ocorre com outros formatos de textura.
-   Algumas das implementações não aplicam a máscara de gravação de saída (D3DRS \_ COLORWRITEENABLE). Aqueles que podem ter máscaras de gravação de cor independentes. Isso é expresso usando um novo bit de recurso. O número de máscaras de gravação de cor independentes disponíveis será igual ao número máximo de elementos dos quais o dispositivo é capaz.
-   [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) limpa todos os elementos da textura de vários elementos que é definida como destino de renderização.

O uso de texturas com vários elementos segue estas etapas:

1.  Os aplicativos detectam suporte para esse recurso verificando a disponibilidade de formatos de textura de vários elementos.
2.  O aplicativo cria essas superfícies chamando [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).
3.  O aplicativo define a superfície como um destino de renderização usando a chamada [**SetRenderTarget**](/windows/desktop/api) . O sombreador de pixel fornece saída para as superfícies usando a instrução [Mov-PS](../direct3dhlsl/mov---ps.md) .
4.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) é chamado para definir uma superfície de textura de vários elementos em um estágio específico. Assim como acontece com outras texturas, a mesma superfície pode ser definida para vários estágios de uma só vez.
5.  [**Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) é chamado para definir D3DSAMP \_ ELEMENTINDEX como o número do elemento apropriado na textura de vários elementos a partir da qual os exemplos de amostra. O valor padrão para esse estado é 0, o que significa que texturas sem vários elementos funcionarão. Definir esse estado como um número inadequado resulta em um comportamento indefinido – se a textura de vários elementos for apenas dois elementos de largura, mas a amostra for solicitada a amostra do quarto elemento, por exemplo.

## <a name="api-support"></a>Suporte a API

Veja a seguir um resumo dos elementos da API que dão suporte a texturas de vários elementos:

-   O formato de superfície [D3DFMT \_ Multi2 \_ ARGB8](d3dformat.md) expressa a natureza intercalada do formato.
-   O \_ estado de amostra D3DSAMP ELEMENTINDEX indica qual índice de elemento usar.
-   Os Estados de renderização a seguir dão suporte a texturas com vários elementos:

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ COLORWRITEENABLE aplica-se ao destino de renderização (ou elemento) zero.

-   O sinalizador [D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md) indica que o dispositivo dá suporte a máscaras de gravação independentes para várias texturas de elementos ou vários destinos de renderização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 
