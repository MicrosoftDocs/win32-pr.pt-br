---
description: Método I LTD::Resume – o método Resume reinicia uma captura em pausa.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: Método I LTD::Resume (Netmon.h)
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
ms.openlocfilehash: dd39cb83c90c566f0022679e70680e916daeb2a43a4d62e993e096930ee2f14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890466"
---
# <a name="iespresume-method"></a>Método I LTD::Resume

O **método Resume** reinicia uma captura em pausa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ NÃO \_ PAUSADA**</dt> </dl> | A captura não está em pausa. Chame [**I LTD::P ause para**](iesp-pause.md) pausar a captura.<br/>                        |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>       | O NPP não está conectado à rede. Chame [**I LTD::Conexão**](iesp-connect.md) para se conectar à rede.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>             | O NPP está conectado à rede, mas não ao [**método I LTD::Conexão.**](iesp-connect.md)<br/>            |



 

## <a name="remarks"></a>Comentários

Enquanto a captura estiver em um estado de pausa, [](c.md) novos dados não serão adicionados ao arquivo de captura atual até que **I REBOOT::Resume** seja chamado para reiniciar a captura. Quando **Pausar** **e Retomar** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.

Ao usar **Pausar** **e Retomar** para controlar a [](c.md) captura, Monitor de Rede continua adicionando estatísticas de conversa às estatísticas existentes para a captura atual.

Para interromper a captura, chame [**I LTD::Stop**](iesp-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[I LTDA](iesp.md)
</dt> <dt>

[**I LTD::Conexão**](iesp-connect.md)
</dt> <dt>

[**I LTD::P ause**](iesp-pause.md)
</dt> <dt>

[**IRIA::Stop**](iesp-stop.md)
</dt> </dl>

 

 




