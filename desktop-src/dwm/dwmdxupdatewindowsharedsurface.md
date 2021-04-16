---
description: Notifica o DWM de uma atualização de entrada para uma superfície compartilhada da janela.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Função DwmDxUpdateWindowSharedSurface
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
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502348"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Função DwmDxUpdateWindowSharedSurface

Notifica o DWM de uma atualização de entrada para uma superfície compartilhada da janela.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Parâmetros

`hwnd`

Um [**HWND**](/windows/desktop/winprog/windows-data-types) que especifica a janela que está sendo atualizada.

`uiUpdateId`

A ID de atualização recuperada de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Reservado.

`hmonitorAssociation`

Reservado.

`prc`

O Rect da janela que está sendo atualizada, no espaço de coordenadas da janela. Um retângulo nulo indica que nenhuma região foi atualizada.

## <a name="return-value"></a>Retornar valor

**S \_ OK** se for bem-sucedido, caso contrário, um HRESULT com falha **.**

## <a name="remarks"></a>Comentários

Essa API destina-se à implementação de um driver de gráficos ou tempo de execução. Um aplicativo pode não chamar esse método. Esta documentação só é válida para o Windows 7, e não há garantia de que essa API exista nem se comporte de maneira semelhante em outras versões do Windows. Essa função não está presente em nenhum cabeçalho ou biblioteca de vínculo estático, e está localizada no ordinal 101 em dwmapi.dll.

Esse método só deve ser chamado depois de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) retornar **S \_ OK** e deve ser chamado nesse cenário, independentemente de a superfície ser atualizada ou não.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | \[Somente aplicativos de área de trabalho do Windows 7\] |
| Servidor mínimo com suporte | Nenhum compatível |
| Fim do suporte do cliente | Windows 7 |
| Cabeçalho | N/D |
| DLL | Dwmapi.dll |
