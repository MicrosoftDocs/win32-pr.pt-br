---
title: MM_MCISIGNAL mensagem (Mmsystem.h)
description: A mensagem MM MCISIGNAL é enviada a uma janela para notificar um aplicativo de que um dispositivo MCI atingiu uma posição definida em um comando \_ MCI SIGNAL (sinal \_ anterior).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb54b56d35ad34d10d95c2a34b52b370fb856d9c958dd42223c7f0a08ddbdfb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807436"
---
# <a name="mm_mcisignal-message"></a>Mensagem \_ MM MCISIGNAL

A **mensagem MM \_ MCISIGNAL** é enviada a uma janela para notificar um aplicativo [](signal.md) de que um dispositivo MCI atingiu uma posição definida em um comando de sinal anterior [**(MCI \_ SIGNAL).**](mci-signal.md)


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*
</dt> <dd>

Identificador do dispositivo que inicia a mensagem de sinal.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valor passado no **membro dwUserParm** da estrutura **\_ MCI DGV \_ SIGNAL \_ PARAMS** quando o comando de sinal definiu essa função de retorno de chamada.  Como alternativa, ele pode conter o valor da posição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Mensagens MCI](mci-messages.md)
</dt> <dt>

[**Sinal**](signal.md)
</dt> </dl>

 

 





