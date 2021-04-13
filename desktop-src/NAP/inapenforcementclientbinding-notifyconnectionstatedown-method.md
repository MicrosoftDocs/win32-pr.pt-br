---
title: Método INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: É usado para informar ao NapAgent que uma conexão com um cliente de imposição foi desativada.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Método NotifyConnectionStateDown NAP
- Método NotifyConnectionStateDown NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método NotifyConnectionStateDown
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
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499856"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>Método INapEnforcementClientBinding:: NotifyConnectionStateDown

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding:: NotifyConnectionStateDown** é usado para informar ao NapAgent que uma conexão a um cliente de imposição foi desativada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*downCxn* \[ no\]
</dt> <dd>

Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão inoperante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O imforçador não foi inicializado anteriormente.<br/>       |



 

## <a name="remarks"></a>Comentários

Quando qualquer uma das conexões estabelecidas por um cliente de imposição for desativada, o cliente de imposição deverá remover a conexão de sua lista ativa e informar o NapAgent usando esse método. Assim que essa chamada retorna, o objeto de conexão pode ser liberado e liberado. O NapAgent não conterá referências ao objeto de conexão.

Como resultado dessa notificação, o NapAgent atualiza seu estado NAP do sistema, conforme apropriado.

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
</dt> </dl>

 

 





