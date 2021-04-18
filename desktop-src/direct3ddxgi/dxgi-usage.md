---
description: Sinalizadores para opções de criação de recursos e superfície.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813594"
---
# <a name="dxgi_usage"></a>uso de DXGI \_

Sinalizadores para opções de criação de recursos e superfície.



| Constante/valor                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**Dxgi \_ \_ \_**</dt> <dt>1L <<  de buffer de fundo de uso (2 + 4)</dt> </dl>                             | A superfície ou o recurso é usado como um buffer de fundo. Você não precisa passar o **\_ buffer de \_ fundo \_ de uso de dxgi** ao criar uma cadeia de permuta. Mas você pode determinar se um recurso pertence a uma cadeia de permuta ao chamar [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e obter **o \_ \_ \_ buffer de fundo de uso de dxgi**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**Dxgi \_ \_Descartar uso \_ no 1L \_ presente**</dt> <dt> <<  (5 + 4)</dt> </dl>       | Esse sinalizador é somente para uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**Dxgi \_ 1L \_ \_ somente leitura de uso**</dt> <dt> <<  (4 + 4)</dt> </dl>                                   | Use a superfície ou o recurso para leitura apenas.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**Dxgi \_ 1L <<  de \_ \_ \_ saída de destino de renderização de uso**</dt> <dt>(1 + 4)</dt> </dl> | Use a superfície ou o recurso como um destino de renderização de saída.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**Dxgi \_ <<  \_ de \_ entrada do sombreador de uso**</dt> <dt>1L (0 + 4)</dt> </dl>                          | Use a superfície ou o recurso como uma entrada para um sombreador.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**Dxgi \_ 1L \_ compartilhado de uso**</dt> <dt> <<  (3 + 4)</dt> </dl>                                             | Compartilhe a superfície ou o recurso.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**Dxgi \_ 1L de \_ \_ acesso não ordenado de uso**</dt> <dt> <<  (6 + 4)</dt> </dl>              | Use a superfície ou o recurso para acesso não ordenado.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Comentários

Cada sinalizador é definido como um inteiro sem sinal.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Essas opções de sinalizador são usadas em uma chamada para o método [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para descrever as opções de uso da superfície e de acesso da CPU para o buffer de fundo de uma cadeia de permuta. Você não pode usar **o \_ uso \_ de dxgi compartilhado**, **\_ \_ descarte \_ de uso de dxgi em diante \_** e os valores de **\_ uso \_ \_ somente leitura de dxgi** como entrada para criar uma cadeia de permuta. No entanto, DXGI pode definir o **\_ \_ descarte \_ de uso de dxgi no \_ momento** e o **uso de dxgi \_ \_ \_ somente leitura** para alguns dos buffers de fundo da cadeia de troca em nome do aplicativo. Você pode chamar o método [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar o uso desses buffers de fundo. A cadeia de permuta só dá suporte ao valor de **\_ \_ \_ nenhum acesso da CPU dxgi** no **\_ campo de \_ acesso \_ à CPU dxgi** da parte do **\_ uso de dxgi**.

Essas opções de sinalizador também são usadas pelo método [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




