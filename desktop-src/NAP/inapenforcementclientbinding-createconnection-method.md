---
title: Método CreateConnection INapEnforcementClientBinding (NapEnforcementClient. h)
description: É usado por imforcers para criar objetos de conexão.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Método CreateConnection NAP
- Método CreateConnection NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Método CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009164"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>Método INapEnforcementClientBinding:: CreateConnection

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de fábrica **INapEnforcementClientBinding:: CreateConnection** é usado por imforcers para criar objetos de conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexão* \[ do fora\]
</dt> <dd>

Um ponteiro COM para uma nova interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) retornada pelo sistema NAP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





