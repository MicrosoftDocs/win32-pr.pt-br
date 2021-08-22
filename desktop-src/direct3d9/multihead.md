---
description: Os cartões de multicabeçalho são aqueles que têm um buffer de quadro comum e acelerador, conversores de digital-to-Analog independentes (DACs) e monitoramento de saídas.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a74f51cea282618c9471eb9a63eedf8eef73c38b4d961209064261a93c4d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563507"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Os cartões de multicabeçalho são aqueles que têm um buffer de quadro comum e acelerador, conversores de digital-to-Analog independentes (DACs) e monitoramento de saídas. Esses dispositivos podem oferecer suporte a vários monitores muito mais utilizáveis do que um número semelhante de adaptadores de vídeo heterogêneos.

Os cartões de vários cabeçotes são expostos na API como um único dispositivo de nível de API que pode gerar várias cadeias de troca de tela inteira. Consequentemente, todos os recursos são compartilhados com todos os cabeçotes, e cada cabeçalho tem exatamente os mesmos recursos. Cada cabeçalho pode ser definido para modos de exibição independentes. Você pode usar chamadas separadas para [**IDirect3DSwapChain9::P reenviada**](/windows/desktop/api) para atualizar cada cabeçalho. Você também pode usar uma chamada para [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para atualizar cada cabeçalho sequencialmente.

> [!Note]  
> A atualização de cada cabeçalho não ocorre simultaneamente com uma única chamada para [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). As estatísticas presentes no Direct3D 9Ex podem usar a estrutura [**D3DPRESENTSTATS**](d3dpresentstats.md) para manter as atualizações para cada cabeçalho perto umas das outras para limitar os efeitos de divisão em vários cabeçotes de adaptadores. Para obter informações sobre a sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip, consulte [melhorias do Direct3d 9EX](../direct3darticles/direct3d-9ex-improvements.md).

 

Cada cadeia de permuta para um dispositivo de multicabeçalho deve ser tela inteira. Quando um dispositivo entra no modo de multitítulo, ele deve permanecer em tela inteira. A transição de volta para o modo de janela requer a destruição do dispositivo (exceto para a operação normal ALT + TAB-to-Minimize).

O método antigo de dividir a memória de vídeo entre os cabeçotes e tratar cada cabeça como um acelerador totalmente independente ainda será um cenário de uso comum. Essa proposta não substitui esse mecanismo, a menos que o aplicativo tenha sido especificamente codificado para funcionar no modo de multicabeçalho do Direct3D 9.

Os drivers recebem conhecimento adequado para alternar entre os dois modos de operação.

Um cabeçalho será chamado de cabeçalho mestre e todos os outros cabeçotes no mesmo cartão serão chamados de cabeçalhos subordinados. Se mais de um adaptador de vários cabeçotes estiver presente em um sistema, o mestre e seus subordinados de um adaptador de vários cabeçalhos serão chamados de grupo. Os grupos são indicados pelo ordinal do adaptador de seu cabeçalho mestre.

A estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) foi atualizada para expor os novos limites de hardware a seguir.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup é 1 para adaptadores convencionais e maior que 1 para o adaptador mestre de um cartão de vários cabeçotes. O valor será 0 para um adaptador subordinado de um cartão de multitítulo. Cada cartão pode ter no máximo um mestre, mas pode ter muitos subordinados.
-   MasterAdapterOrdinal indica qual dispositivo é o mestre para esse subordinado.
-   AdapterOrdinalInGroup indica a ordem na qual os cabeçalhos são referenciados pela API. O adaptador Mestre sempre tem AdapterOrdinalInGroup 0. Esses valores não correspondem aos ordinais do adaptador passados para os métodos IDirect3D9, mas aplicam-se apenas aos cabeçalhos de um grupo.

Essa definição permite que os cartões multitítulo continuem a apresentar vários adaptadores como se fossem cartões independentes, assim como faziam no DirectX 8.

Para criar um dispositivo de multicabeçalho, especifique o sinalizador de comportamento D3DCREATE \_ \_ dispositivo de adaptador de placa em [**IDirect3D9:: CreateDevice**](/windows/desktop/api). Os parâmetros de apresentação (uma matriz [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md)) devem conter elementos NumberOfAdaptersInGroup. O tempo de execução atribuirá cada elemento a cada cabeçalho em ordem numérica AdapterOrdinalInGroup. Quando o \_ dispositivo de \_ grupo de adaptadores D3DCREATE está definido, cada parâmetro de apresentação deve ter:

-   O membro em janela definido como **false** (em outras palavras, seja tela inteira).
-   O mesmo valor para o membro EnableAutoDepthStencil dos [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).

Além disso, se EnableAutoDepthStencil for **true**, cada um dos campos a seguir deverá ter o mesmo valor para cada [**\_ parâmetro D3DPRESENT**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Se o DAC estiver definido, chamadas adicionais para [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) são ilegais.

Se o dispositivo tiver sido criado com o DAC, [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) esperará uma matriz [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).

Cada estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) passada para [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) deve ser tela inteira. Para alternar de volta para o modo em janela, o aplicativo deve destruir o dispositivo e recriar um dispositivo não multicabeçalho no modo de janela.

Este é um cenário de uso básico:


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



Para obter mais informações, consulte [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
