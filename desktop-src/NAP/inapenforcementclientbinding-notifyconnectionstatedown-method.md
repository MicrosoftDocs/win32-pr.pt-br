---
title: Método NotifyConnectionStateDown de INapEnforcementClientBinding (NapEnforcementClient.h)
description: É usado para informar ao NapAgent que uma conexão com um cliente de imposição foi inobada.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Nap do método NotifyConnectionStateDown
- Método NAP NotifyConnectionStateDown, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP , notifyConnectionStateDown método
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e40d3b46e8c970287f49d983d89733d4858e38671ac93fb75d482c0259a73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803046"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>Método INapEnforcementClientBinding::NotifyConnectionStateDown

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientBinding::NotifyConnectionStateDown** é usado para informar o NapAgent de que uma conexão com um cliente de imposição diminuiu.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*downCxn* \[ Em\]
</dt> <dd>

Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão para baixo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite de recursos do sistema, não foi possível executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ NÃO \_ INICIALIZADO**</dt> </dl> | O executor não foi inicializado anteriormente.<br/>       |



 

## <a name="remarks"></a>Comentários

Quando qualquer uma das conexões estabelecidas por um cliente de imposição ficar inativa, o cliente de imposição deverá remover a conexão de sua lista ativa e informar o NapAgent usando esse método. Assim que essa chamada retornar, o objeto de conexão poderá ser liberado e liberado. O NapAgent não conterá referências ao objeto de conexão.

Como resultado dessa notificação, o NapAgent atualiza seu estado NAP do sistema conforme apropriado.

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
</dt> </dl>

 

 





