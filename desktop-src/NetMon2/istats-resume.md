---
description: 'Método IStats:: resume-o método retomar reinicia uma captura pausada.'
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'Método IStats:: resume (Netmon. h)'
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
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114614"
---
# <a name="istatsresume-method"></a>Método IStats:: resume

O método **retomar** reinicia uma captura pausada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>       | O NPP não está conectado à rede.<br/>                                                                                          |
| <dl> <dt>**captura de NMERR \_ \_ não \_ pausada**</dt> </dl> | A captura não está em pausa. Chame o método [IStats::P ause](istats-pause.md) para interromper temporariamente a captura.<br/>                     |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>       | O NPP não está conectado à rede. Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl>     | O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Comentários

Enquanto a captura está em um estado de pausa, novos dados não são capturados até que o método IStats:: resume seja chamado para reiniciar a captura.

Ao usar os métodos **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.

Para interromper a captura, chame [IStats:: Stop](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: conectar](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats:: Stop](istats-stop.md)
</dt> </dl>

 

 




