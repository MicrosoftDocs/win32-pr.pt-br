---
description: Notifica o DWM de uma atualização de entrada para uma superfície compartilhada de janela.
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
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280116"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Função DwmDxUpdateWindowSharedSurface

Notifica o DWM de uma atualização de entrada para uma superfície compartilhada de janela.

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

Um [**HWND que**](/windows/desktop/winprog/windows-data-types) especifica a janela que está sendo atualizada.

`uiUpdateId`

A ID de atualização recuperada [**de DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Reservado.

`hmonitorAssociation`

Reservado.

`prc`

O rect da janela que está sendo atualizada, no espaço de coordenadas da janela. Um retângulo NULL indica que nenhuma região foi atualizada.

## <a name="return-value"></a>Retornar valor

**S \_ OK** se for bem-sucedido, caso contrário, um **HRESULT COM FALHA.**

## <a name="remarks"></a>Comentários

Essa API destina-se à implementação de um driver gráfico ou runtime. Um aplicativo pode não chamar esse método. Esta documentação só é válida para Windows 7 e essa API não tem garantia de existir nem se comportar de maneira semelhante em outras versões do Windows. Essa função não está presente em nenhum título ou biblioteca de link estático e está localizada em ordinal 101 em dwmapi.dll.

Esse método só deve ser chamado depois que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) retornar **S \_ OK** e deve ser chamado nesse cenário, independentemente de a superfície ser atualizada ou não.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 7 \[ aplicativos da área de trabalho\] |
| Servidor mínimo com suporte | Nenhum compatível |
| Fim do suporte ao cliente | Windows 7 |
| Cabeçalho | N/D |
| DLL | Dwmapi.dll |
