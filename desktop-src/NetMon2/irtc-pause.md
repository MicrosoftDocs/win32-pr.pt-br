---
description: Método IRTC::P ause – o método Pause pausa a captura atual.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Método IRTC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1ad7ce342c1e0053622bfb77161ecd1e5d81c25d09af179108065b445dd4dc35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365071"
---
# <a name="irtcpause-method"></a>Método IRTC::P ause

O **método Pause** pausa a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ PAUSADA**</dt> </dl> | A captura já está em pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl>  | O NPP não está capturando dados. Chame [IRTC::Start](irtc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>  | O NPP não está conectado à rede. Chame [IRTC::Conexão](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | O NPP está conectado à rede, mas não ao [método IRTC::Conexão.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Enquanto a captura estiver em um estado de pausa, novos quadros não serão capturados até que o método [IRTC::Resume](irtc-resume.md) seja chamado para reiniciar a captura.

Quando você usa os métodos **IRTC::P ause** e **IRTC::Resume** para controlar a captura, Monitor de Rede continua adicionando estatísticas de [*conversa*](c.md) sempre que a captura está em execução.

Para reiniciar a chamada de captura [IRTC::Resume](irtc-resume.md). Para interromper a captura, chame [IRTC::Stop](irtc-stop.md).

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

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




