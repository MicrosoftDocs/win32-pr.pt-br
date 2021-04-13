---
description: O método pause pausa a captura atual.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: 'IESP: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501344"
---
# <a name="iesppause-method"></a>IESP: método ause de:P

O método **Pause** pausa a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStats* 
</dt> <dd>

Obsoleto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl> | A captura já está em pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>  | O NPP não está capturando dados. Chame [IESP:: Start](iesp-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>  | O NPP não está conectado à rede. Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>        | O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que você chame o método [IESP:: resume](iesp-resume.md) para reiniciar a captura. Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.

Quando você usa os métodos **IESP::P ause** e **IESP:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.

Para reiniciar a captura, chame [IESP:: resume](iesp-resume.md). Para interromper a captura, chame [IESP:: Stop](iesp-stop.md).

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

[IESP:: conectar](iesp-connect.md)
</dt> <dt>

[IESP:: retomar](iesp-resume.md)
</dt> <dt>

[IESP:: iniciar](iesp-start.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




