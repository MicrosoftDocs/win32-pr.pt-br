---
title: Método de inicialização de INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inicializa o SHA (agente de integridade do sistema) e associa o SHA ao serviço NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbe764d477c5f176fcaebc0825bbbcd02495ec70ee669a02c59258173cfbdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802706"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>Método INapSystemHealthAgentBinding:: Initialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentBinding:: Initialize** INICIALIZA o SHA (agente de integridade do sistema) e associa o Sha ao serviço NapAgent. Esse método deve ser chamado antes de chamar qualquer outro método na interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do Sha que está sendo associado ao serviço NapAgent.

</dd> <dt>

*retorno de chamada* \[ no\]
</dt> <dd>

Um ponteiro COM para uma interface [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) usada pelo NapAgent para fazer o retorno de chamada do agente de integridade com uma notificação/processo. O NapAgent mantém uma referência ao objeto associado a essa interface até que [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) seja chamado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                                | Descrição                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Êxito na operação.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Erro de permissões, acesso negado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | O limite de recursos do sistema não pôde executar a operação.<br/>                                                             |
| <dl> <dt>**ERRO \_ já \_ inicializado**</dt> </dl> | Se o SHA tiver sido inicializado anteriormente, esse erro será retornado.<br/>                                                      |
| <dl> <dt>**\_E/s NAP \_ não \_ registradas**</dt> </dl>     | Se o SHA não tiver sido registrado anteriormente, esse erro será retornado.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>        | O NapAgent foi interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.<br/> |



 

## <a name="remarks"></a>Comentários

O NapAgent não dispara uma troca SoH como resultado da inicialização. Um agente de integridade do sistema deve chamar [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para solicitar uma troca de pacotes soh após a inicialização com o NapAgent.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





