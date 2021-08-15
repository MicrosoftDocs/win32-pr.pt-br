---
description: Método IDelaydC::Stop – o método Stop interrompe a captura atual.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: Método IDelaydC::Stop (Netmon.h)
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
ms.openlocfilehash: b5fb6442481574de6732aef1359cf9586b9cdcc1815d9f0b206a1f8a597f1967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365996"
---
# <a name="idelaydcstop-method"></a>Método IDelaydC::Stop

O **método Stop** interrompe a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura STATISTICS](statistics.md) que contém estatísticas de rede, como total de quadros e total de bytes capturados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl> | O NPP não está conectado à rede. Chame [IDelaydC::Conexão](idelaydc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl> | O NPP não está capturando dados. Chame [IDelaydC::Start](idelaydc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ NÃO \_ ATRASADO**</dt> </dl>   | O NPP está conectado à rede, mas não ao [método IDelaydC::Conexão.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Quando **IDelaydC::Stop** é chamado, o Monitor de Rede para de capturar dados e fecha o [*arquivo de captura*](c.md). (O nome do arquivo de captura foi retornado quando [IDelaydC::Start](idelaydc-start.md) foi chamado). Agora você pode ver o conteúdo do arquivo de captura.

Ao parar e iniciar a captura, chame o método [IDelaydC::Configure](idelaydc-configure.md) sempre que chamar [IDelaydC::Start](idelaydc-start.md) para reiniciar a captura.

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

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Estatísticas](statistics.md)
</dt> </dl>

 

 




