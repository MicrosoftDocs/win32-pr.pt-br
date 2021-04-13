---
description: Descreve os parâmetros de apresentação.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Estrutura de D3DPRESENT_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298661"
---
# <a name="d3dpresent_parameters-structure"></a>\_Estrutura de parâmetros D3DPRESENT

Descreve os parâmetros de apresentação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a>Membros

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura dos buffers de fundo da nova cadeia de permuta, em pixels. Se a **janela** for **false** (a apresentação é de tela inteira), esse valor deverá ser igual à largura de um dos modos de exibição enumerados encontrados por meio de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se a **janela** for **true** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área do cliente do **hDeviceWindow** (ou a janela de foco se **hDeviceWindow** for **NULL**) será executada.

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura dos buffers de fundo da nova cadeia de permuta, em pixels. Se a **janela** for **false** (a apresentação é de tela inteira), esse valor deverá ser igual à altura de um dos modos de exibição enumerados encontrados por meio de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se a **janela** for **true** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área do cliente do **hDeviceWindow** (ou a janela de foco se **hDeviceWindow** for **NULL**) será executada.

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

O formato de buffer de fundo. Para obter mais informações sobre formatos, consulte [D3DFORMAT](d3dformat.md). Esse valor deve ser um dos formatos de destino de renderização como validado por [**CheckDeviceType**](/windows/desktop/api). Você pode usar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) para obter o formato atual.

Na verdade, D3DFMT \_ Unknown pode ser especificado para o **BackBufferFormat** enquanto estiver no modo de janela. Isso informa o tempo de execução para usar o formato atual do modo de exibição e elimina a necessidade de chamar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

Para aplicativos em janelas, o formato de buffer de fundo não precisa mais corresponder ao formato de modo de exibição porque a conversão de cores agora pode ser feita pelo hardware (se o hardware oferecer suporte à conversão de cores). O conjunto de possíveis formatos de buffer de fundo é restrito, mas o tempo de execução permitirá que qualquer formato de buffer de fundo válido seja apresentado a qualquer formato de área de trabalho. (Há o requisito adicional de que o dispositivo seja operável na área de trabalho; os dispositivos normalmente não operam em 8 bits por modo de pixel.)

Os aplicativos de tela inteira não podem fazer a conversão de cores.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Esse valor pode ter entre 0 e [D3DPRESENT \_ \_ buffers de fundo \_ máximo](d3dpresent-back-buffers.md) (ou [D3DPRESENT \_ buffers de back-Max, por \_ \_ \_ exemplo](d3dpresent-back-buffers.md) , ao usar o Direct3D 9EX). Os valores de 0 são tratados como 1. Se o número de buffers de fundo não puder ser criado, o tempo de execução falhará na chamada de método e preencherá esse valor com o número de buffers de fundo que podem ser criados. Como resultado, um aplicativo pode chamar o método duas vezes com a mesma \_ estrutura de parâmetros D3DPRESENT e esperar que ela funcione na segunda vez.

O método falhará se não for possível criar um buffer de fundo. O valor de **BackBufferCount** influencia o conjunto de efeitos de permuta permitido. Especificamente, qualquer \_ efeito de troca de cópia D3DSWAPEFFECT requer que haja exatamente um buffer de fundo.

</dd> <dt>

**Multiamostratype**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md)**

</dd> <dd>

Membro do tipo enumerado do [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) . O valor deve ser D3DMULTISAMPLE \_ nenhum, a menos que **SwapEffect** tenha sido definido como \_ descartar D3DSWAPEFFECT. Haverá suporte para multiamostrar apenas se o efeito de permuta for D3DSWAPEFFECT \_ descartar.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nível de qualidade. O intervalo válido é entre zero e um menor que o nível retornado por pQualityLevels usado pelo [**CheckDeviceMultiSampleType**](/windows/desktop/api). Passar um valor maior retorna o erro D3DERR \_ INVALIDCALL. Valores emparelhados de destinos de renderização ou de superfícies de estêncil de profundidade e [**\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md) devem corresponder.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DSWAPEFFECT**](./d3dswapeffect.md) . O tempo de execução garantirá a semântica implícita relacionada ao comportamento de permuta no buffer; Portanto, se a **janela** for **true** e **SwapEffect** for definido como D3DSWAPEFFECT \_ flip, o tempo de execução criará um buffer de fundo extra e copiará o que for o buffer frontal no momento da apresentação.

D3DSWAPEFFECT \_ Copy requer que **BackBufferCount** seja definido como 1.

\_O descarte de D3DSWAPEFFECT será imposto no tempo de execução de depuração preenchendo qualquer buffer com ruído depois que ele for apresentado.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D9 e o Direct3D9Ex<br/> Em Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX é adicionado para designar quando um aplicativo está adotando o modo flip. Ou seja, Whan o quadro de um aplicativo é passado no modo da janela (em vez de copiado) para o Gerenciador de Janelas da Área de Trabalho (DWM) para composição. O modo Inverter fornece largura de banda de memória mais eficiente e permite que um aplicativo aproveite as estatísticas de tela inteira. Ele não altera o comportamento de tela inteira. O comportamento do modo flip está disponível a partir do Windows 7.<br/> |



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

A janela do dispositivo determina o local e o tamanho do buffer de fundo na tela. Isso é usado pelo Direct3D quando o conteúdo do buffer de fundo é copiado para o buffer frontal durante a [**apresentação**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   Para um aplicativo de tela inteira, trata-se de um identificador para a janela superior (que é a janela de foco).

    Para aplicativos que usam vários dispositivos de tela inteira (como um sistema multimonitor), exatamente um dispositivo pode usar a janela de foco como a janela do dispositivo. Todos os outros dispositivos devem ter janelas de dispositivo exclusivas.

-   Para um aplicativo em modo de janela, esse identificador será a janela de destino padrão para o [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Se esse identificador for **nulo**, a janela de foco será tomada.

Observe que nenhuma tentativa é feita pelo tempo de execução para refletir as alterações do usuário no tamanho da janela. O buffer de fundo não é implicitamente redefinido quando esta janela é redefinida. No entanto, o método [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) controla automaticamente as alterações na posição da janela.

</dd> <dt>

**Em janelas**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** se o aplicativo for executado em janela; **False** se o aplicativo for executado em tela inteira.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Se esse valor for **true**, o Direct3D gerenciará buffers de profundidade para o aplicativo. O dispositivo criará um buffer de estêncil de profundidade quando for criado. O buffer de estêncil de profundidade será definido automaticamente como o destino de renderização do dispositivo. Quando o dispositivo for redefinido, o buffer de estêncil de profundidade será automaticamente destruído e recriado no novo tamanho.

Se EnableAutoDepthStencil for **true**, AutoDepthStencilFormat deverá ser um formato de estêncil de profundidade válido.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) . O formato da superfície de estêncil de profundidade automática que o dispositivo criará. Esse membro é ignorado, a menos que **EnableAutoDepthStencil** seja **true**.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Uma das constantes [D3DPRESENTFLAG](d3dpresentflag.md) .

</dd> <dt>

**Tela inteira \_ RefreshRateInHz**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa na qual o adaptador de vídeo atualiza a tela. O valor depende do modo no qual o aplicativo está em execução:

-   Para o modo em janela, a taxa de atualização deve ser 0.
-   Para o modo de tela inteira, a taxa de atualização é uma das taxas de atualização retornadas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa máxima na qual os buffers de fundo da cadeia de troca podem ser apresentados ao buffer frontal. Para obter uma explicação detalhada dos modos e dos intervalos com suporte, consulte [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Existi**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Redefinir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
