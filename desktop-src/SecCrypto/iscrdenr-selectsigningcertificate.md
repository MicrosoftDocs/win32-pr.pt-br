---
description: Exibe uma caixa de diálogo Selecionar certificado, permitindo que um certificado de autenticação (também conhecido como certificado do agente de registro) seja selecionado.
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Método ISCrdEnr:: selectSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836983"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>Método ISCrdEnr:: selectSigningCertificate

O método **selectSigningCertificate** exibe uma caixa de diálogo **Selecionar certificado** , permitindo que um certificado de autenticação (também conhecido como *certificado do agente de registro*) seja selecionado.

Antes de registrar em nome dos usuários, você deve selecionar um certificado de autenticação. A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado de autenticação é usada para assinar uma \# solicitação PKCS 7. O PKCS \# 7, por sua vez, contém a solicitação PKCS \# 10 do usuário (que é assinada com a chave privada do usuário).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
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

Uma cadeia de caracteres que representa o nome do modelo de certificado para o certificado de autenticação. Você pode usar o valor "EnrollmentAgent" se tiver obtido um certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

Se o método for bem sucedido, o método retornará **S \_ OK**.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Antes de registrar em nome de um usuário, primeiro você deve obter um certificado de autenticação. Você pode obter um certificado de autenticação usando o snap-in do MMC do Gerenciador de certificados. O método **selectSigningCertificate** não obtém o certificado de autenticação, mas exibe uma caixa de diálogo de certificados de assinatura obtidos anteriormente, permitindo que você escolha qual certificado será usado para assinar as solicitações de registro em nome.

Uma alternativa para **selectSigningCertificate** é [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).

Depois que um certificado de assinatura é selecionado, seu nome pode ser recuperado chamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

 

 
