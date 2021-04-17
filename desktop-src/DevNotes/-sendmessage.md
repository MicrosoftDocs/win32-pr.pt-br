---
description: Envia a mensagem especificada para uma janela ou Windows.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Função _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748930"
---
# <a name="_sendmessage-function"></a>\_Função SendMessage

\[Essa função é um wrapper sobre a função **SendMessage** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **SendMessage** diretamente.\]

Envia a mensagem especificada para uma janela ou Windows. Consulte [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Sintaxe


```C++
LRESULT _SendMessage(
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

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
