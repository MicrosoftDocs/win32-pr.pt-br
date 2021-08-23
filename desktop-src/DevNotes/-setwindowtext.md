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
ms.openlocfilehash: a0c66230d9e7f074fe50ca826ab196ab75a239942257899362b738296b329074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572546"
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

 

 
