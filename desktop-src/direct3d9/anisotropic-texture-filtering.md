---
description: A distorção visível nos texels de um objeto 3D cuja superfície é orientada em um ângulo em relação ao plano da tela é chamada anisoose.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtragem de textura anisocar (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363aeef463f137a240602e52410260108ee4a40a1a23da7b2e7c245ed6e74a65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676936"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtragem de textura anisocar (Direct3D 9)

A distorção visível nos texels de um objeto 3D cuja superfície é orientada em um ângulo em relação ao plano da tela é chamada anisoose. Quando um pixel de uma primitiva anisotrópica é mapeado para texels, sua forma é distorcida. O Direct3D mede a anisotropia de um pixel como o prolongamento - ou seja, comprimento dividido pela largura - de um pixel de tela é mapeado inverso no espaço de textura.

Você pode usar a filtragem de textura anisotrópica em conjunto com filtragem de textura linear ou a filtragem de textura mipmap para melhorar os resultados da renderização. Seu aplicativo habilita a filtragem de textura anisofatória chamando o [**método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) De definir o valor do primeiro parâmetro para o número do índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura. Passe D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER ou D3DSAMP MIPFILTER para o segundo parâmetro para definir o filtro \_ \_ de ampliação, minificação ou mipmapping. De definir o terceiro parâmetro como D3DTEXF \_ ANIS LTDA.

Seu aplicativo também deve definir o grau de anisopatia como um valor maior que um. Faça isso chamando o [**método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) De definir o valor do primeiro parâmetro como o número do índice inteiro (0-7) da textura para a qual você está definindo o grau de isoção. Passe D3DSAMP \_ MAXPATIASO LTDA como o valor do segundo parâmetro. O parâmetro final deve ser o grau de isoção.

Você pode desabilitar a filtragem de isopatia definindo o grau de isoia como um; qualquer valor maior que um o habilita. Verifique o sinalizador Max Ltda na estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar o possível intervalo de valores para o grau de anisosseia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 
