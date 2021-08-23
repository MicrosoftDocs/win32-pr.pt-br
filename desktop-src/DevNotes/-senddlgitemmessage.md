---
description: Envia uma mensagem para o controle especificado em uma caixa de diálogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage função
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
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538827"
---
# <a name="_senddlgitemmessage-function"></a>\_Função SendDlgItemMessage

\[Essa função é um wrapper sobre a **função SendDlgItemMessage.** Essa função pode ser alterada ou não disponível no futuro. Os aplicativos **devem chamar SendDlgItemMessage** diretamente.\]

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

[**Senddlgitemmessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
