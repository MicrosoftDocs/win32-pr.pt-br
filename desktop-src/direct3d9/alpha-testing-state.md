---
description: Os aplicativos C++ podem usar testes alfa para controlar quando os pixels são gravados na superfície de destino de renderização.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Estado de teste alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b853eb779860d5fc490f4061fde03c852a9c3d9f7bda48baa8e5a84ebd43173c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989436"
---
# <a name="alpha-testing-state-direct3d-9"></a>Estado de teste alfa (Direct3D 9)

Os aplicativos C++ podem usar testes alfa para controlar quando os pixels são gravados na superfície de destino de renderização. Usando o estado de renderização [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , seu aplicativo define o dispositivo Direct3D atual para que ele teste cada pixel de acordo com uma função de teste alfa. Se o teste tiver sucesso, o pixel será gravado na superfície. Caso contrário, o Direct3D ignora o pixel. Selecione a função de teste alfa com o estado de renderização **D3DRS \_ ALPHAFUNC** . Seu aplicativo pode definir um valor alfa de referência para todos os pixels para comparar usando o estado de renderização **D3DRS \_ ALPHAREF** .

O uso mais comum para o teste alfa é melhorar o desempenho ao rasterizar objetos que são quase transparentes. Se os dados de cor que estão sendo rasterizados forem mais opacos do que a cor em um determinado pixel (D3DPCMPCAPS \_ GREATEREQUAL), o pixel será escrito. Caso contrário, o rasterizador ignora completamente o pixel, salvando o processamento necessário para misturar as duas cores. O exemplo de código a seguir verifica se uma determinada função de comparação tem suporte e, em caso afirmativo, define os parâmetros da função de comparação necessários para melhorar o desempenho durante a renderização.


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



Nem todo o hardware dá suporte a todos os recursos de teste alfa. Você pode verificar os recursos do dispositivo chamando o método [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) . Depois de recuperar os recursos do dispositivo, verifique o membro AlphaCmpCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associada para a função de comparação desejada. Se o membro AlphaCmpCaps contiver apenas a \_ capacidade do D3DPCMPCAPS Always ou apenas o D3DPCMPCAPS \_ nunca, o driver não oferecerá suporte a testes alfa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
