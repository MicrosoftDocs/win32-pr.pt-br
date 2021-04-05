---
description: O método Stop interrompe a captura atual.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Método IDelaydC:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460956"
---
# <a name="idelaydcstop-method"></a>Método IDelaydC:: Stop

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



| Código de retorno                                                                                          | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl> | O NPP não está capturando dados. Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não \_ atrasada**</dt> </dl>   | O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Quando **IDelaydC:: Stop** é chamado, monitor de rede para de capturar dados e fecha o [*arquivo de captura*](c.md). (O nome do arquivo de captura foi retornado quando [IDelaydC:: Start](idelaydc-start.md) foi chamado). Agora você pode examinar o conteúdo do arquivo de captura.

Quando você parar e iniciar a captura, certifique-se de chamar o método [IDelaydC:: Configure](idelaydc-configure.md) cada vez que chamar [IDelaydC:: Start](idelaydc-start.md) para reiniciar a captura.

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

[IDelaydC:: conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: configurar](idelaydc-configure.md)
</dt> <dt>

[IDelaydC:: iniciar](idelaydc-start.md)
</dt> <dt>

[ESTATÍSTICA](statistics.md)
</dt> </dl>

 

 




