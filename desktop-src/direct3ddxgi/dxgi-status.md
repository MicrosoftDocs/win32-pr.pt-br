---
description: Códigos de status que podem ser retornados por funções DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765611"
---
# <a name="dxgi_status"></a>STATUS de DXGI \_

Códigos de status que podem ser retornados por funções DXGI.



| Constante/valor                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**Dxgi \_ STATUS \_ obstruído**</dt> <dt>0x087A0001</dt> </dl>                                                 | O conteúdo da janela não está visível. Ao receber esse status, um aplicativo pode parar de renderizar e usar o \_ \_ teste de presente em dxgi para determinar quando retomar a renderização. Você não receberá \_ o status de dxgi \_ obstruído se estiver usando uma cadeia de permuta de modelo invertido.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**Dxgi \_ Modo de STATUS \_ \_ alterado**</dt> <dt>0x087A0007</dt> </dl>                                    | O modo de exibição da área de trabalho foi alterado, pode haver conversão/alongamento de cores. O aplicativo deve chamar [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para corresponder ao novo modo de exibição.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**Dxgi \_ \_ \_ Alteração do modo \_ de status em \_ andamento**</dt> <dt>0x087A0008</dt> </dl> | [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain:: setfullscreenstate**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) retornará \_ \_ \_ a alteração do modo de status dxgi \_ em \_ andamento se uma transição do modo de tela inteira/em janela estiver ocorrendo quando a API for chamada.<br/> |



## <a name="remarks"></a>Comentários

O valor **HRESULT** para cada valor de **\_ status de dxgi** é determinado por essa macro que é definida em DXGItype. h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Por exemplo, **o \_ status \_ de dxgi obstruído** é definido como **0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




