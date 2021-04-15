---
description: A distorção visível no texels de um objeto 3D cuja superfície é orientada a um ângulo em relação ao plano da tela é chamado de anisotropy.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtragem de textura anisotropic (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457132"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtragem de textura anisotropic (Direct3D 9)

A distorção visível no texels de um objeto 3D cuja superfície é orientada a um ângulo em relação ao plano da tela é chamado de anisotropy. Quando um pixel de uma primitiva anisotrópica é mapeado para texels, sua forma é distorcida. O Direct3D mede a anisotropia de um pixel como o prolongamento - ou seja, comprimento dividido pela largura - de um pixel de tela é mapeado inverso no espaço de textura.

Você pode usar a filtragem de textura anisotrópica em conjunto com filtragem de textura linear ou a filtragem de textura mipmap para melhorar os resultados da renderização. Seu aplicativo permite a filtragem de textura anisotropic chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura. Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping. Defina o terceiro parâmetro como D3DTEXF \_ ANISOTROPIC.

Seu aplicativo também deve definir o grau de anisotropy como um valor maior que um. Faça isso chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está definindo o grau de isotropy. Passe D3DSAMP \_ MAXANISOTROPY como o valor do segundo parâmetro. O parâmetro final deve ser o grau de isotropy.

Você pode desabilitar a filtragem de isotropic definindo o grau de isotropy como um; qualquer valor maior que um o habilita. Verifique o sinalizador MaxAnisotropy na estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar o intervalo de valores possível para o grau de anisotropy.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 
