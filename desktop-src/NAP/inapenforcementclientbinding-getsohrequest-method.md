---
title: Método INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: É usado pelo cliente de imposição para recuperar uma solicitação SoH para uma conexão específica.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134332"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>Método INapEnforcementClientBinding:: GetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding:: GetSoHRequest** é usado pelo cliente de imposição para recuperar uma solicitação soh para uma conexão específica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexão* \[ do no\]
</dt> <dd>

Um ponteiro COM para uma interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) . O NapAgent não mantém referências ao objeto associado a essa interface após a conclusão do método.

</dd> <dt>

*retriggerHint* \[ fora\]
</dt> <dd>

Um ponteiro para um **bool** que indica se a conexão deve ser disparada novamente. Será **verdadeiro** se o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) tiver sido alterado desde que essa função foi chamada pela última vez [**ou se o**](nap-datatypes.md) acessador tiver expirado. Caso contrário, **false** será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O imforçador não foi inicializado anteriormente.<br/>       |



 

## <a name="remarks"></a>Comentários

O NapAgent define o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) no objeto de conexão.

Se um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estava pendente nessa conexão, ele é Descartado e os SHAs são notificados de **SoHRequests** órfãos.

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





