---
description: Um mipmap é uma sequência de texturas, cada uma delas é uma representação em resolução mais baixa progressivamente da mesma imagem.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtragem de textura com Mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68f98c1189f130261981fdd309bb3f06bcca1e66f6e23a70e141a5abfe32f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291622"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtragem de textura com Mipmaps (Direct3D 9)

Um mipmap é uma sequência de texturas, cada uma delas é uma representação em resolução mais baixa progressivamente da mesma imagem. A altura e a largura de cada imagem, ou nível, no mipmap é uma potência de dois menores que o nível anterior. Mipmaps não precisam ser quadrados.

Uma imagem de mipmap de alta resolução é usada para objetos que estão próximos ao usuário. Imagens de resolução mais baixa são usadas para o objeto que parece mais distante. O mipmapping melhora a qualidade das texturas renderizadas às custas do uso de mais memória.

O Direct3D representa os mipmaps como uma cadeia de superfícies anexadas. A textura de resolução mais alta fica no topo da cadeia e tem o próximo nível do mipmap como um anexo. Por sua vez, esse nível possui um anexo que é o próximo nível no mipmap e assim por diante, até o nível mais baixo de resolução do mipmap.

As ilustrações a seguir mostram um exemplo desses níveis. As texturas de bitmap representam uma placa em um contêiner em um jogo 3D em primeira pessoa. Quando criada como um mipmap, a textura de resolução mais alta é primeira do conjunto. Cada textura subsequente no conjunto de mipmaps é uma potência de 2 menor em altura e largura. Nesse caso, o mipmap de resolução máxima é de 256 pixels por 256 pixels. A próxima textura é de 128x128. A última textura na cadeia é de 64x64.

Essa placa tem uma distância máxima do qual fica visível. Se o usuário começar distante da placa, o jogo exibirá a textura menor da cadeia de mipmaps, que neste caso é a textura de 64x64.

![ilustração de uma textura de 64x64 de uma placa de perigo](images/mip1.jpg)

Conforme o ponto de vista do usuário se aproxima da placa, as texturas de maior resolução da cadeia de mipmaps são usadas progressivamente. A resolução na ilustração a seguir é de 128x128.

![ilustração de uma textura de 128x128 de uma placa de perigo](images/mip2.jpg)

A textura de resolução mais alta é usada quando o ponto de vista do usuário é a distância mínima permitida de placa, conforme mostrado na ilustração a seguir.

![ilustração de uma textura de 256x256 de uma placa de perigo](images/mip3.jpg)

Essa é uma maneira mais eficiente de simular perspectiva para texturas. Em vez de renderizar uma textura em várias resoluções, é mais rápido usar várias texturas em resoluções variadas.

O Direct3D pode avaliar qual textura de um conjunto de mipmaps tem a resolução mais próxima do resultado desejado e pode mapear pixels para seu espaço de texel. Se a resolução da imagem final é entre as resoluções de texturas no conjunto de mipmaps, o Direct3D pode examinar texels nos dois mipmaps e mesclar seus valores de cor.

Para usar mipmaps, seu aplicativo deve criar um conjunto de mipmaps. Os aplicativos aplicam mipmaps selecionando o conjunto de mipmaps como a primeira textura no conjunto de texturas atuais. Para obter mais informações, consulte [Blending de textura (Direct3D 9)](texture-blending.md).

Em seguida, seu aplicativo deve definir o método de filtragem que o Direct3D usa para fazer a amostragem de texels. O método mais rápido de filtragem de mipmaps é fazer com que o Direct3D selecione o texel mais próximo. Use o valor enumerado D3DTEXF \_ POINT para selecionar isso. O Direct3D poderá produzir melhores resultados de filtragem se seu aplicativo usar o valor \_ enumerado LINEAR D3DTEXF. Isso seleciona o mipmap mais próximo e depois calcula uma média ponderada dos texels ao redor do local na textura para a qual o pixel atual é mapeado.

As texturas de mipmap são usadas em cenas 3D para reduzir o tempo necessário para renderizar uma cena. Eles também melhoram o realismo da cena. No entanto, eles geralmente exigem grandes quantidades de memória.

## <a name="creating-a-set-of-mipmaps"></a>Criando um conjunto de Mipmaps

O exemplo a seguir mostra como seu aplicativo pode chamar o método [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) para criar uma cadeia de cinco níveis de mipmap: 256x256, 128x128, 64x64, 32x32 e 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Os dois primeiros parâmetros aceitos por [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) são o tamanho e a largura da textura de nível superior. O terceiro parâmetro especifica o número de níveis na textura. Se você definir isso como zero, o Direct3D criará uma cadeia de superfícies, cada uma com uma potência menor que a anterior, até o menor tamanho possível de 1x1. O quarto parâmetro especifica o uso desse recurso; nesse caso, 0 é especificado para indicar nenhum uso específico para o recurso. O quinto parâmetro especifica o formato de superfície para a textura. Use um valor do tipo [enumerado D3DFORMAT](d3dformat.md) para esse parâmetro. O sexto parâmetro especifica um membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) que indica a classe de memória na qual colocar o recurso criado. A menos que você esteja usando texturas dinâmicas, o D3DPOOL \_ MANAGED é recomendado. O parâmetro final leva o endereço de um ponteiro para uma interface [**IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

> [!Note]  
> Cada superfície em uma cadeia mipmap tem dimensões que são metade da superfície anterior na cadeia. Se o mipmap de nível superior tiver dimensões de 256x128, as dimensões do mipmap do segundo nível serão de 128 x64, do terceiro nível serão de 64x32 e assim por diante, até 1x1. Você não pode solicitar um número de níveis de mipmap em Níveis que possam fazer com que a largura ou altura de qualquer mipmap da cadeia seja menor que 1. No caso simples de uma superfície de mipmap de nível superior de 4x2, o valor máximo permitido para Níveis é três. As dimensões de nível superior são de 4x2, as dimensões do segundo nível são de 2x1 e as dimensões do terceiro nível são de 1x1. Um valor maior que 3 em Níveis resulta em um valor fracionário na altura do mipmap de segundo nível e, portanto, não permitido.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Selecionando e exibindo um Mipmap

Chame o [**método IDirect3DDevice9::SetTexture**](/windows/desktop/api) para definir o conjunto de texturas mipmap como a primeira textura na lista de texturas atuais. Para obter mais informações, consulte [Blending de textura (Direct3D 9)](texture-blending.md).

Depois que o aplicativo selecionar o conjunto de textura mipmap, ele deverá atribuir valores do tipo enumerado [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) ao estado do amostrador MIPFILTER D3DSAMP. \_ Em seguida, o Direct3D executa automaticamente a filtragem de textura mipmap. A habilitação da filtragem de textura mipmap é demonstrada no exemplo de código a seguir.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



Seu aplicativo também pode percorrer manualmente uma cadeia de superfícies mipmap usando o método [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) e especificando o nível de mipmap a ser recuperado. O exemplo a seguir percorre uma cadeia mipmap das resoluções mais altas para as mais baixas.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Os aplicativos precisam percorrer manualmente uma cadeia mipmap para carregar dados de bitmap em cada superfície na cadeia. Normalmente, esse é o único motivo para percorrer a cadeia. Um aplicativo pode recuperar o número de níveis em um mipmap chamando [**IDirect3DBaseTexture9::GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 
