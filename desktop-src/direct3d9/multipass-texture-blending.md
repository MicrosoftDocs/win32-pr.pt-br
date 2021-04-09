---
description: Os apps Direct3D podem conseguir vários efeitos especiais ao aplicar diversas texturas a um primitivo durante múltiplas passagens de renderização.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Mesclagem de textura de passagem (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087590"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Mesclagem de textura de passagem (Direct3D 9)

Os apps Direct3D podem conseguir vários efeitos especiais ao aplicar diversas texturas a um primitivo durante múltiplas passagens de renderização. O termo comum para isso é mesclagem de texturas de passagem múltipla. O uso típico da mesclagem de textura com passagens múltiplas é emular os efeitos de iluminação complexos e os modelos de sombreamento ao aplicar várias cores de diversas texturas diferentes. Uma dessas aplicações é chamada de mapeamento suave. Para obter mais informações, consulte [mapeamento claro com texturas (Direct3D 9)](light-mapping-with-textures.md).

> [!Note]  
> Alguns dispositivos são capazes de aplicar várias texturas a primitivos em uma única passagem. Para obter detalhes, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md).

 

Se o hardware do usuário não oferecer suporte à mistura de textura múltipla, o app pode usar a mistura de textura com passagem múltipla para obter os mesmo efeitos visuais. No entanto, o app não pode manter as taxas de quadros que são possíveis ao usar a mistura de textura múltipla.

Para executar a mesclagem de textura de passagem em um aplicativo C/C++.

1.  Defina uma textura no estágio de textura 0 chamando o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .
2.  Selecione a cor desejada e os argumentos de mesclagem alfa e as operações com o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . As configurações padrão são adequadas para a mistura de textura com passagem múltipla.
3.  Renderize os objetos adequados na cena.
4.  Defina a textura seguinte no estágio de textura 0.
5.  Defina os \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e D3DRS \_ DESTBLEND para ajustar os fatores de mesclagem de origem e destino, conforme necessário. O sistema combina as novas texturas aos pixels existentes na superfície de destino de renderização de acordo com esses parâmetros.
6.  Repita as etapas 3, 4 e 5 com a quantidade de texturas necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> </dl>

 

 
