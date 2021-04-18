---
description: O método Stop interrompe a captura atual.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'Método IESP:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789514"
---
# <a name="iespstop-method"></a>Método IESP:: Stop

O método **Stop** interrompe a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStats* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de [estatísticas](statistics.md) que contém estatísticas de rede, como total de quadros e total de bytes capturados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl> | O NPP não está capturando dados. Chame [IESP:: Start](iesp-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>       | O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Quando o método **IESP:: Stop** é chamado, monitor de rede para de capturar dados e fecha o [*arquivo de captura.*](c.md) (O nome do arquivo de captura foi retornado quando [IESP:: Start](iesp-start.md) foi chamado.) Agora você pode examinar o conteúdo do arquivo de captura.

Quando você parar e reiniciar a captura, certifique-se de chamar o método [IESP:: Configure](iesp-configure.md) cada vez que chamar [IESP:: Start](iesp-start.md) para reiniciar a captura.

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

[IESP:: iniciar](iesp-start.md)
</dt> <dt>

[ESTATÍSTICA](statistics.md)
</dt> </dl>

 

 




