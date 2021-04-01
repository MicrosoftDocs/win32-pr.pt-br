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
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918591"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





