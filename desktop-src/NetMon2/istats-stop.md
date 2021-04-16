---
description: O método Stop interrompe a captura atual.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'Método IStats:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751410"
---
# <a name="istatsstop-method"></a>Método IStats:: Stop

O método **Stop** interrompe a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>   | O NPP não está conectado à rede. Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>   | O NPP não está capturando dados. Chame o método [IStats:: Start](istats-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl> | O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Comentários

Ao reiniciar a captura após **IStats:: Stop** ter sido chamado, certifique-se de chamar o método [IStats:: Configure](istats-configure.md) cada vez que chamar [IStats:: Start](istats-start.md) para reiniciar a captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: conectar](istats-connect.md)
</dt> <dt>

[IStats:: configurar](istats-configure.md)
</dt> <dt>

[IStats:: iniciar](istats-start.md)
</dt> </dl>

 

 




