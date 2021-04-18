---
description: Os aplicativos podem otimizar qual subconjunto de uma textura é copiado especificando &\# 0034; sujo&\# 0034; regiões em texturas.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Regiões com problemas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810898"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Regiões com problemas de textura (Direct3D 9)

Os aplicativos podem otimizar qual subconjunto de uma textura é copiado especificando regiões "sujas" em texturas. Somente as regiões marcadas como sujas são copiadas por uma chamada para [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture). No entanto, as regiões sujas podem ser expandidas para otimizar o alinhamento. Quando uma textura é criada, toda a textura é considerada suja. Somente as operações a seguir afetam o estado sujo de uma textura:

-   Adicionando uma região suja a uma textura.
-   Bloqueio de algum buffer na textura. Esta operação adiciona a região bloqueada como uma região suja. O aplicativo pode desativar essa atualização de região suja automática se tiver um melhor conhecimento das regiões sujas reais.
-   O uso de um nível de superfície da textura como destino em [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marca a textura inteira como sujo.
-   Usar a textura como uma origem em [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) limpa todas as regiões sujas na textura de origem.
-   Usando [**IDirect3DSurface9:: GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) para retornar um contexto de dispositivo.
-   Chamar [**IDirect3DBaseTexture9:: GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) marca a textura inteira como sujo.
-   Chamar [**IDirect3DBaseTexture9:: SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) marca a textura inteira como sujo.

As regiões sujas são definidas no nível superior de uma textura mipmapped e [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) pode expandir a região suja para baixo na cadeia MIP a fim de minimizar o número de bytes copiados para cada subnível. Observe que as coordenadas de região suja de subnível são arredondadas para fora, ou seja, suas partes fracionárias são arredondadas para a borda mais próxima da textura.

Como cada tipo de textura tem tipos diferentes de regiões sujas, há métodos em cada tipo de textura. as texturas 2D usam o retângulo sujo e as caixas de uso de texturas de volume.

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

A passagem de **NULL** para os parâmetros PDirtyRect ou pDirtyBox para os métodos acima expande a região suja para cobrir toda a textura.

Cada método de bloqueio pode assumir \_ D3DLOCK \_ nenhuma \_ atualização suja, o que impede qualquer alteração no estado sujo da textura. Para obter mais informações, consulte [locking Resources (Direct3D 9)](locking-resources.md).

Quando mais informações sobre o conjunto verdadeiro de regiões que são alteradas durante uma operação de bloqueio estão disponíveis, os aplicativos devem usar D3DLOCK \_ nenhuma \_ \_ atualização suja. Observe que um bloqueio ou uma cópia para um subnível de textura somente (ou seja, sem bloqueio ou cópia para o nível superior) não atualiza as regiões sujas para essa textura. Os aplicativos assumem a mesma responsabilidade de atualizar regiões sujas quando bloqueiam níveis mais baixos sem bloquear o nível mais alto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
