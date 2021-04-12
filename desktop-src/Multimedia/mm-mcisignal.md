---
title: Mensagem de MM_MCISIGNAL (mmsystem. h)
description: A \_ mensagem mm MCISIGNAL é enviada a uma janela para notificar um aplicativo de que um dispositivo MCI atingiu uma posição definida em um comando de sinal anterior ( \_ sinal MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Multimídia do Windows de mensagem MM_MCISIGNAL
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
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369797"
---
# <a name="mm_mcisignal-message"></a>\_Mensagem mm MCISIGNAL

A mensagem **mm \_ MCISIGNAL** é enviada a uma janela para notificar um aplicativo de que um dispositivo MCI atingiu uma posição definida em um comando de [**sinal**](signal.md) anterior ( [**\_ sinal MCI**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Identificador do dispositivo que inicia a mensagem de sinal.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valor passado no membro **dwUserParm** da estrutura de **\_ parâmetros de \_ sinal \_ do MCI DGV** quando o comando de **sinal** definiu essa função de retorno de chamada. Como alternativa, ele pode conter o valor da posição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensagens MCI](mci-messages.md)
</dt> <dt>

[**aviso**](signal.md)
</dt> </dl>

 

 





