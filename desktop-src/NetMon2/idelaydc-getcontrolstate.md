---
description: Método IDelaydC::GetControlState – o método GetControlState recupera o estado da captura, que indica se a captura está em execução ou em pausa.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: Método IDelaydC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 34302215cf0e773d7713f56233d38462071f1dde725a85478688cfb9ca2a4f45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365889"
---
# <a name="idelaydcgetcontrolstate-method"></a>Método IDelaydC::GetControlState

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



| Código de retorno                                                                                          | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl> | O NPP não está conectado à rede. Chame [IDelaydC::Conexão](idelaydc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO \_ ATRASADO**</dt> </dl>   | O NPP está conectado à rede, mas não ao [método IDelaydC::Conexão.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado sempre que o NPP estiver conectado à rede usando a interface [IDelaydC.](idelaydc.md) Você pode usar esse método para descobrir se uma captura está em execução, se a captura está em pausa ou se a captura foi interrompida, mas o NPP não está desconectado.

Os métodos usados para iniciar, pausar e interromper a captura são listados na lista Consulte Também abaixo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conexão](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




