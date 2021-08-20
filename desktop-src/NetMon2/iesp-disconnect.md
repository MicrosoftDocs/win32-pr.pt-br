---
description: 'IESP: método isconnect:D-o método Disconnect desconecta o NPP da rede.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: 'IESP: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14ea098c27d4a16a74c03928b924eb77ee0eee8fa1a674d29fd8c3bd71aefdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981220"
---
# <a name="iespdisconnect-method"></a>Método IESP::D isconnect

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



| Código de retorno                                                                                          | Descrição                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>      | O NPP está capturando dados. Não é possível desconectar da rede enquanto a captura de dados está em andamento.<br/> |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede.<br/>                                                             |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>       | o NPP está conectado à rede, mas não com o método [IESP:: Conexão](iesp-connect.md) .<br/>       |



 

## <a name="remarks"></a>Comentários

Este método não pode ser chamado quando o NPP está capturando dados. Você deve chamar o método **IESP:: Stop** antes de chamar **IESP::D isconnect**.

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

[IESP:: Conexão](iesp-connect.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




