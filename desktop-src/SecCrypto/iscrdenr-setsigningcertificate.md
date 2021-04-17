---
description: Especifica um certificado de autenticação (também conhecido como o certificado do agente de registro).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Método ISCrdEnr:: setSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755043"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>Método ISCrdEnr:: setSigningCertificate

O método **setSigningCertificate** especifica um certificado de autenticação (também conhecido como o *certificado do agente de registro*).

Antes de registrar em nome dos usuários, você deve selecionar ou definir um certificado de autenticação. A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado de autenticação é usada para assinar uma \# solicitação PKCS 7. O PKCS \# 7, por sua vez, contém a solicitação PKCS \# 10 do usuário (que é assinada com a chave privada do usuário).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado para uso futuro. Defina esse valor como zero.

</dd> <dt>

*bstrCertTemplateName* \[ no\]
</dt> <dd>

Nome do modelo de certificado para o certificado de autenticação. Você pode usar o valor "EnrollmentAgent" se tiver obtido um certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Antes de registrar em nome de um usuário, primeiro você deve obter um certificado de autenticação. Você pode obter um certificado de autenticação usando o snap-in do MMC do Gerenciador de certificados. O método **setSigningCertificate** não obtém o certificado de autenticação, mas informa ao controle de registro de cartão inteligente que anteriormente obteve o certificado de autenticação a ser usado. O método **setSigningCertificate** pesquisa o repositório "My" do chamador para o certificado de autenticação mais recente correspondente ao modelo de certificado especificado por *bstrCertTemplateName*.

Uma alternativa para **setSigningCertificate** é **ISCrdEnr:: setSigningCertificate**.

Depois que um certificado de assinatura é definido, seu nome pode ser recuperado chamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
