---
description: Método IDelaydC::P ause – o método Pause pausa a captura atual.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Método IDelaydC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: dfe48afce1e8fd2350f1d1b696eb426a326ade1b30151e872afee30c0ed997f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910506"
---
# <a name="idelaydcpause-method"></a>Método IDelaydC::P ause

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



| Código de retorno                                                                                           | Descrição                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ PAUSADA**</dt> </dl> | A captura já está em um estado de pausa.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl>  | O NPP não está capturando dados. Chame [IDelaydC::Start](idelaydc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>  | O NPP não está conectado à rede. Chame [IDelaydC::Conexão](idelaydc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO \_ ATRASADO**</dt> </dl>    | O NPP está conectado à rede, mas não ao [método IDelaydC::Conexão.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Enquanto a captura estiver em um estado de pausa, [](c.md) novos dados não serão adicionados ao arquivo de captura atual até que o método **IDelaydC::Resume** seja chamado para reiniciar a captura. Quando **Pausar** **e Retomar** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.

Ao usar **IDelaydC::P ause** e **IDelaydC::Resume** para controlar a captura, Monitor de Rede continua adicionando estatísticas de [*conversa*](c.md) sempre que a captura estiver em execução.

Para reiniciar a captura, chame [IDelaydC::Resume](idelaydc-resume.md).

Para interromper a captura, chame [IDelaydC::Stop](idelaydc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conexão](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




