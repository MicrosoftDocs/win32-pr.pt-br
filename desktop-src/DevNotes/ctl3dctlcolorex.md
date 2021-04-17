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
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752773"
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

## <a name="return-value"></a>Retornar valor

Retorna um identificador para o pincel apropriado se a função tiver sucesso; caso contrário, ele retorna `(HBRUSH)(0)` indicando que ocorreu um erro.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
