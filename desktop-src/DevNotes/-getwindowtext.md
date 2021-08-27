---
description: Recupera o texto da barra de título da janela especificada.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: _GetWindowText função
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
ms.openlocfilehash: 0da23649b52593db1274ebfe36d928c6a7b0a7a244bebae17cc5e720c8dc6093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087986"
---
# <a name="_getwindowtext-function"></a>\_Função GetWindowText

\[Essa função é um wrapper sobre a **função GetWindowText.** Essa função pode ser alterada ou não disponível no futuro. Os aplicativos devem **chamar GetWindowText** diretamente.\]

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

[**Getwindowtext**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
