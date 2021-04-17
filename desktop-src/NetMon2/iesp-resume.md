---
description: O método retomar reinicia uma captura pausada.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'Método IESP:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759671"
---
# <a name="iespresume-method"></a>Método IESP:: resume

O método **retomar** reinicia uma captura pausada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ não \_ pausada**</dt> </dl> | A captura não está em pausa. Chame [**IESP::P ause**](iesp-pause.md) para pausar a captura.<br/>                        |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>       | O NPP não está conectado à rede. Chame [**IESP:: Connect**](iesp-connect.md) para conectar-se à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>             | O NPP está conectado à rede, mas não com o método [**IESP:: Connect**](iesp-connect.md) .<br/>            |



 

## <a name="remarks"></a>Comentários

Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que **IESP:: resume** seja chamado para reiniciar a captura. Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.

Ao usar **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.

Para interromper a captura, chame [**IESP:: Stop**](iesp-stop.md).

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

[**IESP:: conectar**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> </dl>

 

 




