---
description: O método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'Método IRTC:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827866"
---
# <a name="irtcgetcontrolstate-method"></a>Método IRTC:: getcontrolstate

O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsRunnning* \[ fora\]
</dt> <dd>

Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.

</dd> <dt>

*IsPaused* \[ fora\]
</dt> <dd>

Indicador de que a captura atual está em pausa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>  | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado sempre que o NPP estiver conectado à rede. Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP ainda está conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




