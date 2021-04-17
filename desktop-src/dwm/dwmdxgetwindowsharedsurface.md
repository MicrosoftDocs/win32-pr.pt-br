---
description: Recupera a superfície compartilhada do DirectX fazendo backup de uma determinada janela. Essa superfície pode ser gravada para atualizar o conteúdo da janela.
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
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766415"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>Função DwmDxGetWindowSharedSurface

Recupera a superfície compartilhada do DirectX fazendo backup de uma determinada janela. Essa superfície pode ser gravada para atualizar o conteúdo da janela.

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

O [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) do adaptador em que a superfície deve ser localizada.

`hmonitorAssociation`

Reservado.

`dwFlags`

Esse parâmetro pode ser um dos valores a seguir, ou uma combinação de bits ou de vários valores, quando apropriado.

| Valor | Significado |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ Sinalizador de redirecionamento de \_ \_ espera**</dt> <dt>0</dt> </dl> | Faz com que a função seja bloqueada até que uma sincronização vertical (VSync) tenha passado desde a última vez que a função foi chamada com êxito. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ Suporte ao sinalizador de redirecionamento \_ \_ \_ presente \_ na \_ \_ superfície do GDI**</dt> <dt>0x10</dt> </dl> | Indica que o aplicativo de chamada é capaz de apresentar a uma superfície compartilhada GDI. |

`pfmtWindow`

Na entrada, o formato desejado da superfície. Na saída, o formato real da superfície retornada.

`phDxSurface`

Na saída, o identificador compartilhado para a superfície.

`puiUpdateId`

Na saída, a ID da atualização.

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.

| Código de retorno | Descrição |
|-|-|
| **S \_ OK** | A chamada foi bem-sucedida, e você deve atualizar a superfície, passando a ID de atualização para [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (no membro **PresentHistoryToken** da estrutura de **\_ renderização D3DKMT** quando a atualização é enviada e, em seguida, [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve ser chamado com a mesma ID de atualização. Observe que **DwmDxUpdateWindowSharedSurface** deve ser chamado independentemente de a superfície ter sido realmente atualizada ou não. |
| **\_superfície de \_ \_ redirecionamento GDI do DWM S \_** | A chamada foi bem-sucedida e você deve atualizar a superfície chamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e definindo o **modelo** do membro **PRESENTHISTORYTOKEN** como **D3DKMT \_ PM \_ Redirecionado \_ BLT** e fornecendo a ID de atualização no membro **BLT** da União. Esse valor só será retornado se **o \_ suporte a sinalizador de redirecionamento \_ \_ de DWM \_ presente \_ para a \_ \_ superfície GDI** tiver sido especificado em *dwFlags*. |
| **DWM \_ E \_ adaptador \_ não \_ encontrados** | O valor de *luidAdapter* não é válido. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | O DWM não está habilitado no momento e o aplicativo precisará apresentar outra maneira. |

## <a name="remarks"></a>Comentários

Essa API destina-se à implementação de um driver de gráficos ou tempo de execução. Um aplicativo pode não chamar esse método. Esta documentação só é válida para o Windows 7, e não há garantia de que essa API exista nem se comporte de maneira semelhante em outras versões do Windows. Essa função não está presente em nenhum cabeçalho ou biblioteca de vínculo estático, e está localizada no ordinal 100 em dwmapi.dll.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | \[Somente aplicativos de área de trabalho do Windows 7\] |
| Servidor mínimo com suporte | Nenhum compatível |
| Fim do suporte do cliente | Windows 7 |
| Cabeçalho | N/D |
| DLL | Dwmapi.dll |
