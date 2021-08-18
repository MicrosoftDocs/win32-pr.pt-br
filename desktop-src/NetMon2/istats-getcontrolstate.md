---
description: Método IStats::GetControlState – o método GetControlState recupera o estado da captura, que indica se a captura está em execução ou em pausa.
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: Método IStats::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5dcc0ea5a7278364218bde23fbffdfa720070c9a54dbff0feb20abc1f161d024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063826"
---
# <a name="istatsgetcontrolstate-method"></a>Método IStats::GetControlState

O **método GetControlState** recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsRunnning* \[ out\]
</dt> <dd>

Indicador de que a captura atual está em execução, incluindo se a captura estiver em pausa.

</dd> <dt>

*IsPaused* \[ out\]
</dt> <dd>

Indicador de que a captura atual está em pausa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>   | O NPP não está conectado à rede. Chame [IStats::Conexão](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO \_ APENAS \_ ESTATÍSTICAS**</dt> </dl> | O NPP está conectado à rede, mas não ao método [IStats::Conexão.](istats-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado sempre que o NPP estiver conectado à rede. Você pode usar esse método para descobrir se uma captura está em execução, se a captura está em pausa ou se a captura foi interrompida, mas o NPP não está desconectado.

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

[IStatsC::Start](istats-start.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




