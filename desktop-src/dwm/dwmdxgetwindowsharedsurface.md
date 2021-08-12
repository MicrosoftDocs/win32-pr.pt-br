---
description: Recupera a superfície compartilhada do DirectX que dá o backing de uma determinada janela. Essa superfície pode ser escrita para atualizar o conteúdo da janela.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Função DwmDxGetWindowSharedSurface
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 47f8c75ee55521c0f1da4151f5161cf44a63dc51aab5658edbca288cb8edce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280126"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>Função DwmDxGetWindowSharedSurface

Recupera a superfície compartilhada do DirectX que dá o backing de uma determinada janela. Essa superfície pode ser escrita para atualizar o conteúdo da janela.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>Parâmetros

`hwnd`

Um [**HWND**](/windows/desktop/winprog/windows-data-types) que especifica a janela a ser atualizada.

`luidAdapter`

O [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) do adaptador em que a superfície deve estar localizada.

`hmonitorAssociation`

Reservado.

`dwFlags`

Esse parâmetro pode ser um dos valores a seguir ou uma combinação OR bit a bit de vários valores, quando apropriado.

| Valor | Significado |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ SINALIZADOR DE \_ \_ REDIRECIONAMENTO WAIT**</dt> <dt>0</dt> </dl> | Faz com que a função bloqueie até que uma sincronização vertical (VSync) tenha passado desde a última vez em que a função foi chamada com êxito. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ SUPORTE AO \_ SINALIZADOR \_ DE \_ REDIRECIONAMENTO PRESENTE NO \_ \_ GDI \_ SURFACE**</dt> <dt>0X10</dt> </dl> | Indica que o aplicativo de chamada é capaz de apresentar a uma superfície compartilhada GDI. |

`pfmtWindow`

Na entrada, o formato desejado da superfície. Na saída, o formato real da superfície retornada.

`phDxSurface`

Na saída, o alça compartilhada para a superfície.

`puiUpdateId`

Na saída, a ID da atualização.

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.

| Código de retorno | Descrição |
|-|-|
| **S \_ OK** | A chamada foi bem-sucedida e você deve atualizar a superfície, passando a ID de atualização para [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (no membro **PresentHistoryToken** da estrutura **RENDER D3DKMT \_** quando a atualização é enviada e, em seguida, [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve ser chamado com a mesma ID de atualização. Observe que **DwmDxUpdateWindowSharedSurface** deve ser chamado, independentemente de a superfície ter sido realmente atualizada ou não. |
| **SUPERFÍCIE DE \_ \_ REDIRECIONAMENTO GDI da \_ DWM S \_** | A chamada foi bem-sucedida e você deve atualizar a superfície chamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e definindo o Modelo do membro **PresentHistoryToken** como **D3DKMT \_ PM \_ REDIRECTED \_ BLT** e fornecendo a ID de atualização no **membro Blt** da união.  Esse valor só será retornado se **o SINALIZADOR DE REDIRECIONAMENTO DWM \_ DAR SUPORTE PRESENTE À SUPERFÍCIE \_ \_ \_ \_ \_ GDI \_** foi especificado *em dwFlags*. |
| **ADAPTADOR DWM \_ E \_ NÃO \_ \_ ENCONTRADO** | O valor de *luidAdapter* não é válido. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | A DWM não está habilitada no momento e o aplicativo precisará apresentar outra maneira. |

## <a name="remarks"></a>Comentários

Essa API destina-se à implementação de um driver gráfico ou runtime. Um aplicativo pode não chamar esse método. Esta documentação só é válida para Windows 7 e essa API não tem garantia de existir nem se comportar de maneira semelhante em outras versões do Windows. Essa função não está presente em nenhum título ou biblioteca de link estático e está localizada em ordinal 100 em dwmapi.dll.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 7 \[ aplicativos da área de trabalho\] |
| Servidor mínimo com suporte | Nenhum compatível |
| Fim do suporte ao cliente | Windows 7 |
| Cabeçalho | N/D |
| DLL | Dwmapi.dll |
