---
title: Método INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtém uma lista de terceiras partes confiáveis que se inscreveram.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Método GetSubscribedRelyingParties NAP
- Método GetSubscribedRelyingParties NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, método GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454737"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>Método INapCertRelyingParty:: GetSubscribedRelyingParties

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetSubscribedRelyingParties** Obtém uma lista de terceiras partes confiáveis que se inscreveram.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de fora\]
</dt> <dd>

Um ponteiro para um [**EnforcementEntityCount**](nap-datatypes.md) que contém o número de terceiras partes confiáveis assinadas.

</dd> <dt>

*relyingParties* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**EnforcementEntityId**](nap-datatypes.md) que contém a lista de terceiras partes confiáveis inscritas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O chamador deve liberar o parâmetro *relyingParties* usando **CoTaskMemFree**.

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

 

 





