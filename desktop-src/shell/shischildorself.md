---
UID: ''
title: Função SHIsChildOrSelf
description: Compara se uma janela é igual a, um filho de ou um descendente de, uma segunda janela.
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
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941326"
---
# <a name="shischildorself-function"></a>Função SHIsChildOrSelf

## <a name="description"></a>Descrição

\[Essa função está disponível por meio Windows XP e Windows Server 2003.
Ele pode ser alterado ou não disponível nas versões subsequentes do Windows.\]

Compara se uma janela é igual a, um filho de ou um descendente de, uma segunda janela.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parâmetros

### <a name="hwndparent-in"></a>hwndParent [in]

Digite: **HWND**

Um alça para a primeira janela.

### <a name="hwnd-in"></a>hwnd [in]

Digite: **HWND**

Um alça para uma janela a ser testada em *relação a hwndParent.*

## <a name="returns"></a>Retornos

Tipo: **HRESULT**

Retorna **S_OK** se a janela especificada por *hwnd* for igual a, um filho de ou um descendente da janela especificada por *hwndParent*.
Retornará **S_FALSE** se a janela especificada por hwnd não for igual a, não um filho de e não um descendente da janela especificada por *hwndParent*.
O valor de retorno será indefinido se qualquer alça de janela for inválida.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
