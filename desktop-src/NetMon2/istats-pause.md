---
description: O método pause interrompe temporariamente a captura atual.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: 'IStats: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759188"
---
# <a name="istatspause-method"></a>IStats: método ause de:P

O método **Pause** interrompe temporariamente a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl>  | A captura já está em pausa.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>   | O NPP não está capturando dados. Chame o método [IStats:: Start](istats-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>   | O NPP não está conectado à rede. Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl> | O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Comentários

Enquanto a captura é pausada, novos quadros não são capturados até que uma chamada para o método [IStats:: resume](istats-resume.md) reinicie a captura.

Quando você usa os métodos **IStats::P ause** e **IStats:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.

Para reiniciar a chamada de captura [IStats:: resume](istats-resume.md). Para interromper a captura, chame [IStats:: Stop](istats-stop.md).

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

[IStats:: retomar](istats-resume.md)
</dt> <dt>

[IStats:: iniciar](istats-start.md)
</dt> <dt>

[IStats:: Stop](istats-stop.md)
</dt> </dl>

 

 




