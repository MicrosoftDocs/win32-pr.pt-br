---
description: Chamado quando o registro de uma janela do Shell é revogado.
title: Método DShellWindowsEvents.WindowRevoked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459843"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>Método DShellWindowsEvents.WindowRevoked

Chamado quando o registro de uma janela do Shell é revogado.

## <a name="syntax"></a>Sintaxe


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lCookie* \[ Em\]
</dt> <dd>

Tipo: **Inteiro**

O cookie que identifica a janela que foi revogada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Uma janela é concedida a um cookie quando ele é registrado como uma janela do Shell. Para obter mais informações, consulte [**Registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produto<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Revogar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




