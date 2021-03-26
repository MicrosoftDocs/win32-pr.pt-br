---
UID: ''
title: Função SHIsChildOrSelf
description: Compara se uma janela é igual a, um filho de ou um descendente de uma segunda janela.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104988639"
---
# <a name="shischildorself-function"></a>Função SHIsChildOrSelf

## <a name="description"></a>Description

\[Essa função está disponível por meio do Windows XP e do Windows Server 2003.
Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Compara se uma janela é igual a, um filho de ou um descendente de uma segunda janela.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parâmetros

### <a name="hwndparent-in"></a>hwndParent [in]

Tipo: **HWND**

Um identificador para a primeira janela.

### <a name="hwnd-in"></a>HWND [in]

Tipo: **HWND**

Um identificador para uma janela a ser testado em relação a *hwndParent*.

## <a name="returns"></a>Retornos

Tipo: **HRESULT**

Retorna **S_OK** se a janela especificada por *HWND* é igual a, um filho de ou um descendente da janela especificada por *hwndParent*.
Retorna **S_FALSE** se a janela especificada por HWND não for igual a, não um filho de, e não um descendente da janela especificada por *hwndParent*.
O valor de retorno será indefinido se o identificador da janela for inválido.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
