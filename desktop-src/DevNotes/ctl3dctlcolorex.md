---
description: Manipula a mensagem do WM \_ CTLCOLOR para aplicativos que usam o ctl3d.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Função Ctl3dCtlColorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691636"
---
# <a name="ctl3dctlcolorex-function"></a>Função Ctl3dCtlColorEx

Manipula a mensagem do **WM \_ CTLCOLOR** para aplicativos que usam o ctl3d.

## <a name="syntax"></a>Sintaxe


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wm* 
</dt> <dd>

A mensagem do **WM \_ CTLCOLOR** para o aplicativo.

</dd> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto de exibição (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para uma janela filho (controle).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um identificador para o pincel apropriado se a função tiver sucesso; caso contrário, ele retorna `(HBRUSH)(0)` indicando que ocorreu um erro.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
