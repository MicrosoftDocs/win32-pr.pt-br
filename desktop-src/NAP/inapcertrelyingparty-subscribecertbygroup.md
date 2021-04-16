---
title: Método INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Assina um servidor de certificado de integridade (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Método SubscribeCertByGroup NAP
- Método SubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751172"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>Método INapCertRelyingParty:: SubscribeCertByGroup

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **SubscribeCertByGroup** assina um servidor de certificado de integridade (HCS). O HCS já deve estar registrado antes da assinatura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

 *ID* \[ em\]
</dt> <dd>

Um [**EnforcementEntityId**](nap-datatypes.md) que contém a ID do cliente de imposição que está se inscrevendo.

</dd> <dt>

*SubscriberName* \[ no\]
</dt> <dd>

O nome do assinante.

> [!Note]  
> Atualmente, isso é usado apenas para fins de log.

 

</dd> <dt>

*reservado* \[ para no\]
</dt> <dd>

Deve ser **NULL**.

</dd> <dt>

*certExists* \[ fora\]
</dt> <dd>

Indica se um certificado de integridade deste HCS já está sendo mantido pelo NapAgent e está presente no repositório de computadores. Se for **true**, um certificado de integridade já estará sendo mantido e estará presente. Se for **false**, um certificado de integridade não estará sendo mantido e estará presente no momento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





