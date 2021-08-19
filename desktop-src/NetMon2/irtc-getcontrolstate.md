---
description: Método IRTC::GetControlState – o método GetControlState recupera o estado da captura, que indica se a captura está em execução ou pausada.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: Método IRTC::GetControlState (Netmon.h)
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
ms.openlocfilehash: bf3f4b70f1b06f5f985d459af361dc27f320d84465f5ef86f2d956339bf90ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778786"
---
# <a name="irtcgetcontrolstate-method"></a>Método IRTC::GetControlState

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



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl> | O NPP não está conectado à rede. Chame [IRTC::Conexão](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | O NPP está conectado à rede, mas não ao [método IRTC::Conexão.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado sempre que o NPP estiver conectado à rede. Você pode usar esse método para descobrir se uma captura está em execução, se a captura está em pausa ou se a captura foi interrompida, mas o NPP ainda está conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Conexão](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




