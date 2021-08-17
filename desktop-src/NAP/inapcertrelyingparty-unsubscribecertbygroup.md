---
title: Método INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Cancela a assinatura de um servidor de certificado de integridade (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Método UnSubscribeCertByGroup NAP
- Método UnSubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8b9f5398ba63c0e6108adfefd51d0546180db4536dbd95615e5b15dddde523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940214"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>Método INapCertRelyingParty:: UnSubscribeCertByGroup

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **UnSubscribeCertByGroup** cancela a assinatura de um servidor de certificado de integridade (HCS).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

 *ID* \[ em\]
</dt> <dd>

Um [**EnforcementEntityId**](nap-datatypes.md) que contém a ID do cliente de imposição que está sendo cancelado.

</dd> <dt>

 *reservado* \[ para no\]
</dt> <dd>

Deve ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Se não houver nenhum outro assinante para o HCS, o NapAgent excluirá os certificados de integridade correspondentes do repositório do computador local.

Antes de chamar esse método, chame [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





