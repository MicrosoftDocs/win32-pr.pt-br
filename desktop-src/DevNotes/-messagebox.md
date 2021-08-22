---
description: Cria, exibe e opera uma caixa de mensagem.
ms.assetid: ec444595-da2a-4c73-a472-3820983f7303
title: _MessageBox função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MessageBox
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 7bdc1da33b6b2ca0c917637a77ce381469aa5afbc1848d47dd89fd2dc94f9b1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956184"
---
# <a name="_messagebox-function"></a>\_Função MessageBox

\[Essa função é um wrapper sobre a **função MessageBox.** Essa função pode ser alterada ou não disponível no futuro. Os aplicativos devem **chamar MessageBox** diretamente.\]

Cria, exibe e opera uma caixa de mensagem. Consulte [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox).

## <a name="syntax"></a>Sintaxe


```C++
int _MessageBox(
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

[**Messagebox**](/windows/win32/api/winuser/nf-winuser-messagebox)
</dt> </dl>

 

 
