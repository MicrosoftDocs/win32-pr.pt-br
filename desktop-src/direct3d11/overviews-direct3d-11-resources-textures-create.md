---
title: Como criar uma textura
description: Este tópico mostra como criar uma textura.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6539caec121f301dd89906f7cd78134d3b7cd79083c0d185af63d488ef1648eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565546"
---
# <a name="how-to-create-a-texture"></a>Como criar uma textura

A maneira mais simples de criar uma textura é descrever suas propriedades e chamar a API de criação de textura. Este tópico mostra como criar uma textura.

**Para criar uma textura**

1.  Preencha uma estrutura [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) com uma descrição dos parâmetros de textura.
2.  Crie a textura chamando [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) com a descrição da textura.

Este exemplo cria uma textura de 256 x 256, com uso dinâmico [**,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)para uso como um recurso de sombreador com acesso de gravação [**de CPU**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag). [](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




