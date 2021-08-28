---
description: Os aplicativos podem otimizar qual subconjunto de uma textura é copiado especificando &\# 0034;dirty&\# 0034; regiões em texturas.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Regiões sujas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e1aee2980fcf6f3483bf4bf77a53b2515c5a6c28a4c834e65d8c884f941f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092146"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Regiões sujas de textura (Direct3D 9)

Os aplicativos podem otimizar qual subconjunto de uma textura é copiado especificando regiões "sujas" em texturas. Somente as regiões marcadas como sujas são copiadas por uma chamada para [**IDirect3DDevice9::UpdateTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) No entanto, as regiões sujas podem ser expandidas para otimizar o alinhamento. Quando uma textura é criada, toda a textura é considerada suja. Somente as seguintes operações afetam o estado sujo de uma textura:

-   Adicionar uma região suja a uma textura.
-   Bloquear algum buffer na textura. Essa operação adiciona a região bloqueada como uma região suja. O aplicativo poderá desativar essa atualização automática de região suja se tiver um melhor conhecimento das regiões sujas reais.
-   Usar um nível de superfície da textura como destino [**em IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marca toda a textura como suja.
-   Usar a textura como fonte [**em IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) limpa todas as regiões sujas na textura de origem.
-   Usando [**IDirect3DSurface9::GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) para retornar um contexto de dispositivo.
-   Chamar [**IDirect3DBaseTexture9::GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) marca toda a textura como suja.
-   Chamar [**IDirect3DBaseTexture9::SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) marca toda a textura como suja.

As regiões sujas são definidas no nível superior de uma textura mapeada e [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) pode expandir a região suja pela cadeia mip para minimizar o número de bytes copiados para cada subnível. Observe que as coordenadas de região suja de subnível são arredondadas para fora, ou seja, suas partes fracionadas são arredondadas para a borda mais próxima da textura.

Como cada tipo de textura tem diferentes tipos de regiões sujas, há métodos em cada tipo de textura. Texturas 2D usam retângulo sujo e texturas de volume usam caixas.

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Passar **NULL** para os parâmetros pDirtyRect ou pDirtyBox para os métodos acima expande a região suja para cobrir toda a textura.

Cada método de bloqueio pode usar D3DLOCK NO DIRTY UPDATE, o que impede qualquer alteração \_ no estado sujo da \_ \_ textura. Para obter mais informações, [consulte Locking Resources (Direct3D 9)](locking-resources.md).

Quando mais informações sobre o verdadeiro conjunto de regiões que são alteradas durante uma operação de bloqueio estão disponíveis, os aplicativos devem usar D3DLOCK \_ NO \_ DIRTY \_ UPDATE. Observe que um bloqueio ou uma cópia somente para um subnível de textura (ou seja, sem bloqueio ou cópia para o nível superior) não atualiza as regiões sujas para essa textura. Os aplicativos assumem a mesma responsabilidade por atualizar regiões sujas quando eles bloquearem níveis inferiores sem bloquear o nível mais alto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
