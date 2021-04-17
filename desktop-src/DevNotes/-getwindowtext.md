---
description: Recupera o texto da barra de título da janela especificada.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: Função _GetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747464"
---
# <a name="_getwindowtext-function"></a>\_Função GetWindowText

\[Essa função é um wrapper sobre a função **GetWindowText** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **GetWindowText** diretamente.\]

Recupera o texto da barra de título da janela especificada. Consulte [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).

## <a name="syntax"></a>Sintaxe


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
