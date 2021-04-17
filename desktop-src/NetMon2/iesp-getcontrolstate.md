---
description: O método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'Método IESP:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c791d5dc1f5d5321268fef2fb5cf91e04d9ecff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779973"
---
# <a name="iespgetcontrolstate-method"></a>Método IESP:: getcontrolstate

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
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>       | O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .<br/>                     |



 

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

[IESP](iesp.md)
</dt> <dt>

[IESP:: conectar](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP:: iniciar](iesp-start.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




