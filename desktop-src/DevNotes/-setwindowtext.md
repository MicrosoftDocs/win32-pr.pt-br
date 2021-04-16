---
description: Altera o texto da barra de título da janela especificada (se tiver uma).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: Função _SetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752395"
---
# <a name="_setwindowtext-function"></a>\_Função SetWindowText

\[Essa função é um wrapper sobre a função **SetWindowText** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **SetWindowText** diretamente.\]

Altera o texto da barra de título da janela especificada (se tiver uma). Consulte [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).

## <a name="syntax"></a>Sintaxe


```C++
BOOL _SetWindowText(
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

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
