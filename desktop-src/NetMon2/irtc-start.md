---
description: O método Start inicia a captura.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Método IRTC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827862"
---
# <a name="irtcstart-method"></a>Método IRTC:: Start

O método **Start** inicia a captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl> | A captura está em um estado de pausa e deve ser interrompida para que possa ser reiniciada. Chame [IRTC:: Stop](idelaydc-stop.md) para interromper a captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | A captura já foi iniciada.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>  | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/>                         |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>   | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                                             |



 

## <a name="remarks"></a>Comentários

Ao reiniciar a captura usando os métodos IRTC:: Start e [IRTC:: Stop](irtc-stop.md) , você deve chamar o método [IRTC:: Configure](irtc-configure.md) para reconfigurar a conexão cada vez que chamar IRTC:: Start para reiniciar a captura de dados.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [IRTC::P ause](irtc-pause.md) e [IRTC:: resume](irtc-resume.md) .

 

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

[IRTC:: configurar](irtc-configure.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: retomar](irtc-resume.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




