---
description: Códigos de status que podem ser retornados por funções DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2151c2c209feb630dfe445af2f5afc9d20048c08872fc73f9f5388abc5abb4b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951226"
---
# <a name="dxgi_status"></a>STATUS DO DXGI \_

Códigos de status que podem ser retornados por funções DXGI.



| Constante/valor                                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ STATUS \_ OCLUÍDO**</dt> <dt>0X087A0001</dt> </dl>                                                 | O conteúdo da janela não está visível. Ao receber esse status, um aplicativo pode parar de renderizar e usar DXGI \_ PRESENT TEST para determinar quando retomar a \_ renderização. Você não receberá STATUS DO DXGI OCCLUDED se estiver usando uma cadeia de troca de \_ \_ modelo in flip.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ MODO DE STATUS \_ \_ ALTERADO**</dt> <dt>0X087A0007</dt> </dl>                                    | O modo de exibição da área de trabalho foi alterado, pode haver conversão/alongamento de cores. O aplicativo deve chamar [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para corresponder ao novo modo de exibição.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ ALTERAÇÃO \_ NO MODO DE STATUS EM ANDAMENTO \_ \_ \_ 0X087A0008**</dt> <dt></dt> </dl> | [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) retornarão ALTERAÇÃO NO MODO DE STATUS DO DXGI EM ANDAMENTO se uma transição de modo em tela \_ \_ \_ \_ inteira/janela estiver ocorrendo quando qualquer \_ API for chamada.<br/> |



## <a name="remarks"></a>Comentários

O **valor HRESULT** para cada **valor DE \_ STATUS DXGI** é determinado nessa macro que é definida em DXGItype.h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Por exemplo, **STATUS DXGI \_ \_ OCCLUDED** é definido **como 0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




