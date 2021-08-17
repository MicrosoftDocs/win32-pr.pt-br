---
description: Sinalizadores para opções de criação de recursos e superfície.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7bc0773794c6c2243d8a3171cbd6ffdafbe1cdd558e1198c2c8cc0b1a3440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909927"
---
# <a name="dxgi_usage"></a>USO DO \_ DXGI

Sinalizadores para opções de criação de recursos e superfície.



| Constante/valor                                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ BUFFER \_ DE \_ BACK DE**</dt> USO <dt>1L << (2 + 4)</dt> </dl>                             | A superfície ou o recurso é usado como um buffer de fundo. Você não precisa passar o BUFFER DE BACK **DE USO do DXGI \_ \_ \_** ao criar uma cadeia de permuta. Mas você pode determinar se um recurso pertence a uma cadeia de permuta ao chamar [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e obter BUFFER DE BACK DE USO **do DXGI \_ \_ \_**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ DESCARTE \_ DE USO NO \_ \_ ATUAL**</dt> <dt>1L << (5 + 4)</dt> </dl>       | Esse sinalizador é somente para uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ USO \_ SOMENTE \_ LEITURA**</dt> <dt>1L << (4 + 4)</dt> </dl>                                   | Use a superfície ou o recurso para somente leitura.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ SAÍDA \_ \_ DE DESTINO DE \_ RENDERIZAÇÃO**</dt> <dt>DE USO 1L << (1 + 4)</dt> </dl> | Use a superfície ou o recurso como um destino de renderização de saída.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ ENTRADA \_ DO \_ SOMBREADOR DE**</dt> USO <dt>1L << (0 + 4)</dt> </dl>                          | Use a superfície ou o recurso como uma entrada para um sombreador.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ USO \_ COMPARTILHADO**</dt> <dt>1L << (3 + 4)</dt> </dl>                                             | Compartilhe a superfície ou o recurso.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ USO \_ ACESSO NÃO \_ ORGANIZADO**</dt> <dt>1L << (6 + 4)</dt> </dl>              | Use a superfície ou o recurso para acesso não organizado.<br/>                                                                                                                                                                                                                                                                    |



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

Essas opções de sinalizador são usadas em uma chamada para o método [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para descrever o uso da superfície e as opções de acesso à CPU para o buffer de fundo de uma cadeia de troca. Não é possível usar os valores **DXGI \_ USAGE \_ SHARED,** **DXGI \_ USAGE DISCARD \_ ON \_ \_ PRESENT** e **DXGI \_ USAGE READ \_ \_ ONLY** como entrada para criar uma cadeia de permuta. No entanto, o DXGI pode definir DESCARTE DE USO **DXGI ON \_ \_ \_ \_ PRESENT** e **DXGI \_ USAGE READ \_ \_ ONLY** para alguns dos buffers de back da cadeia de permuta em nome do aplicativo. Você pode chamar o [**método IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar o uso desses buffers de fundo. A cadeia de permuta só dá suporte ao valor DE ACESSO À **CPU DXGI \_ \_ \_ NONE** na parte CAMPO DE ACESSO da **CPU DXGI \_ \_ \_** do **USO do \_ DXGI.**

Essas opções de sinalizador também são usadas pelo [**método IDXGIDevice::CreateSurface.**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




