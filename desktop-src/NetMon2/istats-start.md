---
description: O método Start inicia uma captura.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'Método IStats:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827347"
---
# <a name="istatsstart-method"></a>Método IStats:: Start

O método **Start** inicia uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl>  | A captura foi pausada e deve ser interrompida para que possa ser reiniciada. Chame o método [IStats:: Stop](istats-stop.md) para interromper a captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>        | A captura já foi iniciada.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>   | O NPP não está conectado à rede. Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.<br/>           |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl> | O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .<br/>                                          |



 

## <a name="remarks"></a>Comentários

Ao reiniciar a captura usando os métodos IStats:: Start e [IStats:: Stop](istats-stop.md) , você deve chamar o método [IStats:: Configure](istats-configure.md) para reconfigurar a conexão cada vez que chamar IStats:: Start para reiniciar a captura de dados.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [IStats::P ause](istats-pause.md) e [IStats:: resume](istats-resume.md) . Quando você usa esses métodos, os dados capturados são armazenados no mesmo arquivo de captura.

 

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

[IStats:: configurar](istats-configure.md)
</dt> <dt>

[IStats:: conectar](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats:: retomar](istats-resume.md)
</dt> <dt>

[IStats:: Stop](istats-stop.md)
</dt> </dl>

 

 




