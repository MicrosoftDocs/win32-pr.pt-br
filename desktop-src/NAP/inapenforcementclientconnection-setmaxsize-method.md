---
title: Método setmaxsize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Define o tamanho máximo do pacote SoH para esse cliente.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Método setmaxsize NAP
- Método setmaxsize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método setmaxsize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c487e26b89fbc53376837e59fdcc7c298b71ebb10ffc3e2490036b536f28264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781016"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a>Método INapEnforcementClientConnection:: setmaxsize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: setmaxsize** define o tamanho máximo do pacote soh para esse cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxSize* \[ no\]
</dt> <dd>

Uma estrutura [**ProtocolMaxSize**](nap-datatypes.md) que indica o tamanho máximo, em bytes, do pacote soh.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é definido pelo cliente de imposição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





