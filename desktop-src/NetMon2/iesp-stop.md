---
description: Método I LTD::Stop – o método Stop interrompe a captura atual.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: Método I LTD::Stop (Netmon.h)
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
ms.openlocfilehash: d22333bcaad688fa9ebb805857db3673f48e70591e1d8953274598acef2b368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037506"
---
# <a name="iespstop-method"></a>Método I LTD::Stop

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



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl> | O NPP não está conectado à rede. Chame [I LTD::Conexão](iesp-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl> | O NPP não está capturando dados. Chame [I LTD::Start](iesp-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>       | O NPP está conectado à rede, mas não ao [método I LTD::Conexão.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentários

Quando o **método I LTD::Stop** é chamado, Monitor de Rede interrompe a captura de dados e fecha o [*arquivo de captura.*](c.md) (O nome do arquivo de captura foi retornado quando [I LTD::Start](iesp-start.md) foi chamado.) Agora você pode ver o conteúdo do arquivo de captura.

Ao parar e reiniciar a captura, certifique-se de chamar o método [I REBOOT::Configure](iesp-configure.md) sempre que você chamar [I REBOOT::Start](iesp-start.md) para reiniciar a captura.

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

[I LTD::Conexão](iesp-connect.md)
</dt> <dt>

[I LTD::Start](iesp-start.md)
</dt> <dt>

[Estatísticas](statistics.md)
</dt> </dl>

 

 




