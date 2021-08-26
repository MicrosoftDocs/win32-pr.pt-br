---
description: Método IStats::Start – o método Start inicia uma captura.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: Método IStats::Start (Netmon.h)
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
ms.openlocfilehash: 494ec12a0bb9c5c312f34e9cc53e82bfcbe155f90c38b98b2ba807e9c87b6945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037146"
---
# <a name="istatsstart-method"></a>Método IStats::Start

O **método Start** inicia uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ PAUSADA**</dt> </dl>  | A captura foi pausada e deve ser interrompida antes que possa ser reiniciada. Chame o [método IStats::Stop](istats-stop.md) para interromper a captura.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>        | A captura já foi iniciada.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>   | O NPP não está conectado à rede. Chame o [método IStats::Conexão](istats-connect.md) para conectar o NPP à rede.<br/>           |
| <dl> <dt>**NMERR \_ NÃO \_ APENAS \_ ESTATÍSTICAS**</dt> </dl> | O NPP está conectado à rede, mas não ao método [IStats::Conexão.](istats-connect.md)<br/>                                          |



 

## <a name="remarks"></a>Comentários

Ao reiniciar a captura usando os métodos IStats::Start e [IStats::Stop,](istats-stop.md) você deve chamar o método [IStats::Configure](istats-configure.md) para reconfigurar a conexão sempre que chamar IStats::Start para reiniciar a captura de dados.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [IStats::P ause](istats-pause.md) e [IStats::Resume.](istats-resume.md) Quando você usa esses métodos, os dados capturados são armazenados no mesmo arquivo de captura.

 

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

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Conexão](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




