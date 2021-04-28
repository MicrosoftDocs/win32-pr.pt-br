---
description: IRTC::P método ause-o método pause pausa a captura atual.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: 'IRTC: método ause de:P (Netmon. h)'
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
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110674"
---
# <a name="irtcpause-method"></a>IRTC: método ause de:P

O método **Pause** pausa a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl> | A captura já está em pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>  | O NPP não está capturando dados. Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>  | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>   | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Enquanto a captura está em um estado de pausa, novos quadros não são capturados até que o método [IRTC:: resume](irtc-resume.md) seja chamado para reiniciar a captura.

Quando você usa os métodos **IRTC::P ause** e **IRTC:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.

Para reiniciar a chamada de captura [IRTC:: resume](irtc-resume.md). Para interromper a captura, chame [IRTC:: Stop](irtc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC:: retomar](irtc-resume.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




