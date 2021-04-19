---
description: Envia uma mensagem para o controle especificado em uma caixa de diálogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: Função _SendDlgItemMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755636"
---
# <a name="_senddlgitemmessage-function"></a>\_Função SendDlgItemMessage

\[Essa função é um wrapper sobre a função **SendDlgItemMessage** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **SendDlgItemMessage** diretamente.\]

Envia uma mensagem para o controle especificado em uma caixa de diálogo. Consulte [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).

## <a name="syntax"></a>Sintaxe


```C++
LRESULT _SendDlgItemMessage(
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

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
