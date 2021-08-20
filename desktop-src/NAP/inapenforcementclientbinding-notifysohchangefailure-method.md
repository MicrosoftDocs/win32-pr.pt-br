---
title: Método NotifySoHChangeFailure INapEnforcementClientBinding (NapEnforcementClient.h)
description: É usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um INapEnforcementClientCallback NotifySoHChange anterior.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Nap do método NotifySoHChangeFailure
- NotifySoHChangeFailure método NAP , interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP , notifySoHChangeFailure method
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f91ae79656ec8909a8bff041e3ddc2714f1cbd17a65362e08731e9ca411d57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134214"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>Método INapEnforcementClientBinding::NotifySoHChangeFailure

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding::NotifySoHChangeFailure** é usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite de recursos do sistema, não foi possível executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ NÃO \_ INICIALIZADO**</dt> </dl> | O executor não foi inicializado anteriormente.<br/>       |



 

## <a name="remarks"></a>Comentários

Como resultado desse método, o NapAgent repetirá a aplicação da alteração do SoH posteriormente chamando [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) novamente. Depois que o cliente de imposição tiver chamado [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), ele deverá aplicar a alteração, ou seja, nenhuma falha será tratada pelo NapAgent após esse ponto.

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





