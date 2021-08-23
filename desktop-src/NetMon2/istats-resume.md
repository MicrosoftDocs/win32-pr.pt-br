---
description: Método IStats::Resume – o método Resume reinicia uma captura em pausa.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: Método IStats::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 72c73107ea4bf4662d4251a7c9e06ed1844feca88cb0ce6700887e65f6f08021
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063816"
---
# <a name="istatsresume-method"></a>Método IStats::Resume

O **método Resume** reinicia uma captura em pausa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>       | O NPP não está conectado à rede.<br/>                                                                                          |
| <dl> <dt>**CAPTURA NMERR \_ \_ NÃO \_ PAUSADA**</dt> </dl> | A captura não está em pausa. Chame o [método IStats::P ause](istats-pause.md) para interromper temporariamente a captura.<br/>                     |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>       | O NPP não está conectado à rede. Chame o [método IStats::Conexão](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO \_ APENAS \_ ESTATÍSTICAS**</dt> </dl>     | O NPP está conectado à rede, mas não ao método [IStats::Conexão.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Comentários

Enquanto a captura estiver em um estado de pausa, novos dados não serão capturados até que o método IStats::Resume seja chamado para reiniciar a captura.

Ao usar os  **métodos Pausar** e Retomar para controlar [](c.md) a captura, Monitor de Rede continua adicionando estatísticas de conversa às estatísticas existentes para a captura atual.

Para interromper a captura, chame [IStats::Stop](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Conexão](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




