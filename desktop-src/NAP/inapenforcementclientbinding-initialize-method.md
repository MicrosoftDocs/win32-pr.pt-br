---
title: Método de inicialização de INapEnforcementClientBinding (NapEnforcementClient. h)
description: Inicia o serviço NapAgent automaticamente.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454907"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>Método INapEnforcementClientBinding:: Initialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding:: Initialize** inicia o serviço NapAgent automaticamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [**EnforcementEntityId**](nap-datatypes.md) que identifica o cliente de imposição e sua versão.

</dd> <dt>

*retorno de chamada* \[ no\]
</dt> <dd>

Um ponteiro COM para uma interface [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) usada pelo NapAgent para fazer o retorno de chamada dos clientes de imposição com notificação/processo. O NapAgent mantém uma referência ao objeto associado a essa interface até que [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) seja chamado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                                         | Descrição                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                               | A operação teve êxito.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>                     | Erro de permissões, acesso negado.<br/>                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                      | O limite de recursos do sistema não pôde executar a operação.<br/>                       |
| <dl> <dt>**HRESULT (erro \_ já \_ inicializado)**</dt> </dl> | Se o aplicador tiver sido inicializado anteriormente, esse código de erro será retornado.<br/> |
| <dl> <dt>**\_E/s NAP \_ não \_ registradas**</dt> </dl>              | Se o imforçador não tiver sido registrado anteriormente, esse código de erro será retornado.<br/>      |



 

## <a name="remarks"></a>Comentários

O cliente de imposição deve chamar o método **INapEnforcementClientBinding:: Initialize** antes de chamar qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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

[**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





