---
description: Desconecta o NPP da rede.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: 'IStats: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: eabba7b5cf234d48b2839074ec1ad07380a7ed14858f6bd43b07f7d2eaa033b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037186"
---
# <a name="istatsdisconnect-method"></a>Método IStats::D isconnect

O método **Disconnect desconecta** o NPP da rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>        | O NPP está capturando dados no momento. Não é possível desconectar da rede enquanto uma captura de dados está em andamento.<br/> |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>   | O NPP não está conectado à rede.<br/>                                                                         |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl> | o NPP está conectado à rede, mas não com o método [**IStats:: Conexão**](istats-connect.md) .<br/>          |



 

## <a name="remarks"></a>Comentários

Este método não pode ser chamado quando o NPP está capturando dados. Chame o método **IStats::D isconnect** primeiro e, em seguida, chame [**IStats:: Stop**](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats:: Conexão**](istats-connect.md)
</dt> <dt>

[**IStats:: Stop**](istats-stop.md)
</dt> </dl>

 

 




