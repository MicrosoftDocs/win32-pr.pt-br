---
description: Descreve os parâmetros de apresentação.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS estrutura (D3D9Types.h)
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
ms.openlocfilehash: 543b6b40d3fe24f902eb999a9377b8dbf60e1baa31efb70febbd2c0261d47305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857436"
---
# <a name="d3dpresent_parameters-structure"></a>Estrutura D3DPRESENT \_ PARAMETERS

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura dos buffers de fundo da nova cadeia de permuta, em pixels. Se **Windowed** for **FALSE** (a apresentação é de tela inteira), esse valor deverá ser igual à largura de um dos modos de exibição enumerados encontrados por [**meio de EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se **Windowed** for **TRUE** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área de cliente **do hDeviceWindow** (ou a janela de foco, se **hDeviceWindow for** **NULL**) será tomada.

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura dos buffers de fundo da nova cadeia de permuta, em pixels. Se **Windowed** for **FALSE** (a apresentação é de tela inteira), esse valor deverá ser igual à altura de um dos modos de exibição enumerados encontrados por [**meio de EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se **Windowed** for **TRUE** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área de cliente **do hDeviceWindow** (ou a janela de foco, se **hDeviceWindow for** **NULL**) será tomada.

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

O formato de buffer de fundo. Para obter mais informações sobre formatos, [consulte D3DFORMAT](d3dformat.md). Esse valor deve ser um dos formatos de destino de renderização, conforme validado por [**CheckDeviceType**](/windows/desktop/api). Você pode usar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) para obter o formato atual.

Na verdade, D3DFMT UNKNOWN pode ser especificado \_ para **o BackBufferFormat** enquanto estiver no modo em janelas. Isso informa ao runtime para usar o formato de modo de exibição atual e elimina a necessidade de [**chamar GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

Para aplicativos em janelas, o formato de buffer de fundo não precisa mais corresponder ao formato de modo de exibição porque a conversão de cores agora pode ser feita pelo hardware (se o hardware dá suporte à conversão de cores). O conjunto de formatos de buffer de fundo possíveis é restrito, mas o runtime permitirá que qualquer formato de buffer de fundo válido seja apresentado a qualquer formato de área de trabalho. (Há o requisito adicional de que o dispositivo seja operável na área de trabalho; os dispositivos normalmente não operam em 8 bits por modo de pixel.)

Os aplicativos de tela inteira não podem fazer a conversão de cores.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Esse valor pode estar entre 0 e [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (ou [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) ao usar Direct3D 9Ex). Os valores de 0 são tratados como 1. Se o número de buffers de fundo não puder ser criado, o runtime falhará na chamada do método e preencherá esse valor com o número de buffers de fundo que podem ser criados. Como resultado, um aplicativo pode chamar o método duas vezes com a mesma estrutura D3DPRESENT PARAMETERS e esperar que ele \_ funcione na segunda vez.

O método falhará se um buffer de fundo não puder ser criado. O valor de **BackBufferCount** influencia qual conjunto de efeitos de permuta são permitidos. Especificamente, qualquer efeito de troca D3DSWAPEFFECT \_ COPY requer que haja exatamente um buffer de fundo.

</dd> <dt>

**Multisampletype**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) O valor deve ser D3DMULTISAMPLE NONE, a menos que \_ **SwapEffect** tenha sido definido como D3DSWAPEFFECT \_ DISCARD. Multisampling só será suportado se o efeito de permuta for D3DSWAPEFFECT \_ DISCARD.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nível de qualidade. O intervalo válido está entre zero e um menor que o nível retornado por pQualityLevels usado por [**CheckDeviceMultiSampleType**](/windows/desktop/api). Passar um valor maior retorna o erro D3DERR \_ INVALIDCALL. Valores emparelhados de destinos de renderização ou de superfícies de estêncil de profundidade e [**D3DMULTISAMPLE \_ TYPE devem**](./d3dmultisample-type.md) corresponder.

</dd> <dt>

**Swapeffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DSWAPEFFECT.**](./d3dswapeffect.md) O runtime garantirá a semântica implícita sobre o comportamento de troca de buffer; portanto, se **Windowed** for **TRUE** e **SwapEffect** estiver definido como D3DSWAPEFFECT FLIP, o runtime criará um buffer de back extra e copiará o que se tornar o buffer frontal no momento da \_ apresentação.

D3DSWAPEFFECT \_ COPY requer que **BackBufferCount** seja definido como 1.

D3DSWAPEFFECT DISCARD será imposto no runtime de depuração preenchendo qualquer buffer com ruído \_ depois que ele for apresentado.

Diferenças entre Direct3D9 e Direct3D9Ex:

- No Direct3D9Ex, D3DSWAPEFFECT FLIPEX é adicionado para designar quando um \_ aplicativo está adotando o modo de in flip. Ou seja, o quadro de um aplicativo é passado no modo da janela (em vez de copiado) para o Gerenciador de Janelas da Área de Trabalho(DWM) para composição. O modo de invasão fornece largura de banda de memória mais eficiente e permite que um aplicativo aproveite as estatísticas presentes na tela inteira. Ele não altera o comportamento de tela inteira. O comportamento do modo de in flip está disponível a partir do Windows 7.



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

A janela do dispositivo determina o local e o tamanho do buffer de fundo na tela. Isso é usado pelo Direct3D quando o conteúdo do buffer de fundo é copiado para o buffer frontal durante [**o Present.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)

-   Para um aplicativo de tela inteira, esse é um lidar com a janela superior (que é a janela de foco).

    Para aplicativos que usam vários dispositivos de tela inteira (como um sistema multimonitor), exatamente um dispositivo pode usar a janela de foco como a janela do dispositivo. Todos os outros dispositivos devem ter janelas de dispositivo exclusivas.

-   Para um aplicativo de modo de janela, esse handle será a janela de destino padrão para [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Se esse alça for **NULL,** a janela de foco será usada.

Observe que nenhuma tentativa é feita pelo runtime para refletir as alterações do usuário no tamanho da janela. O buffer de fundo não é redefinido implicitamente quando essa janela é redefinida. No entanto, o [**método Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) acompanha automaticamente as alterações de posição da janela.

</dd> <dt>

**Janela**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** se o aplicativo for executado em janelas; **FALSE** se o aplicativo for executado em tela inteira.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Se esse valor for **TRUE,** o Direct3D gerenciará buffers de profundidade para o aplicativo. O dispositivo criará um buffer de estêncil de profundidade quando ele for criado. O buffer de estêncil de profundidade será definido automaticamente como o destino de renderização do dispositivo. Quando o dispositivo for redefinido, o buffer de estêncil de profundidade será destruído e recriado automaticamente no novo tamanho.

Se EnableAutoDepthStencil for **TRUE,** AutoDepthStencilFormat deverá ser um formato válido de estêncil de profundidade.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo [enumerado D3DFORMAT.](d3dformat.md) O formato da superfície de estêncil de profundidade automática que o dispositivo criará. Esse membro é ignorado, a menos **que EnableAutoDepthStencil** seja **TRUE.**

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Uma das constantes [D3DPRESENTFLAG.](d3dpresentflag.md)

</dd> <dt>

**RefreshRateInHz de FullScreen \_**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa na qual o adaptador de exibição atualiza a tela. O valor depende do modo no qual o aplicativo está em execução:

-   Para o modo em janelas, a taxa de atualização deve ser 0.
-   Para o modo de tela inteira, a taxa de atualização é uma das taxas de atualização retornadas por [**EnumAdapterModes.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa máxima na qual os buffers de fundo da cadeia de permuta podem ser apresentados ao buffer frontal. Para uma explicação detalhada dos modos e dos intervalos com suporte, consulte [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Createdevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Redefinir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
