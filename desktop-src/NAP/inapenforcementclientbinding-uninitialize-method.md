---
title: Método Uninitialize do INapEnforcementClientBinding (NapEnforcementClient. h)
description: Conclui o serviço NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Método Uninitialize NAP
- Método Uninitialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787389"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>Método INapEnforcementClientBinding:: Uninitialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding:: Uninitialize** conclui o serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O NapAgent bloqueia o processamento adicional até que todas as chamadas existentes nas interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) e [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) sejam concluídas. No final desta chamada, o NapAgent libera Todas as suas referências em ponteiros COM do cliente de imposição.

Antes que essa função seja chamada, o aplicador deve chamar [**INapEnforcementClientBinding:: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) em todas as suas conexões ativas, para que os SHAs possam ser notificados se qualquer um dos seus SoH-Requests estavam órfãos.

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

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





