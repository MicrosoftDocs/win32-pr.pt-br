---
description: O método retomar reinicia uma captura pausada.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Método IDelaydC:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646789"
---
# <a name="idelaydcresume-method"></a>Método IDelaydC:: resume

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



| Código de retorno                                                                                                | Descrição                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ não \_ pausada**</dt> </dl> | A captura não está em pausa. Chame [**IDelaydC::P ause**](idelaydc-pause.md) para pausar a captura.<br/>                                |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>       | O NPP não está conectado à rede. Chame [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ atrasada**</dt> </dl>         | O NPP está conectado à rede, mas não com o método [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Enquanto a captura é pausada, novos dados não são adicionados ao [*arquivo de captura*](c.md) atual até que o método **IDelaydC:: resume** seja chamado para reiniciar a captura. Quando [**Pause**](idelaydc-pause.md) e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.

Ao usar [**Pause**](idelaydc-pause.md) e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.

Para interromper a captura, chame [**IDelaydC:: Stop**](idelaydc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC:: conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




