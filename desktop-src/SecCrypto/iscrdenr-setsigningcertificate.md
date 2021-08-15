---
description: Especifica um certificado de assinatura (também conhecido como certificado do agente de registro).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: Método ISCrdEnr::setSigningCertificate
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
ms.openlocfilehash: 8b93e2b76e46ed75abcd6460f351dfc2780826c2ff5e7dc8d07e8d48ae617e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425726"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>Método ISCrdEnr::setSigningCertificate

O **método setSigningCertificate** especifica um certificado de assinatura (também conhecido como certificado *do agente de registro*).

Antes de se registrar em nome dos usuários, você deve selecionar ou definir um certificado de assinatura. A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado de assinatura é usada para assinar uma solicitação PKCS \# 7. O PKCS 7, por sua vez, contém a solicitação \# PKCS 10 do usuário (que é assinada com a \# chave privada do usuário).

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

*dwFlags* \[ Em\]
</dt> <dd>

Reservado para uso futuro. De definir esse valor como zero.

</dd> <dt>

*bstrCertTemplateName* \[ Em\]
</dt> <dd>

Nome do modelo de certificado para o certificado de assinatura. Você poderá usar o valor "EnrollmentAgent" se tiver obtido um certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="vb"></a>VB

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

## <a name="remarks"></a>Comentários

Antes de se registrar em nome de um usuário, primeiro você deve obter um certificado de assinatura. Você pode obter um certificado de assinatura usando o snap-in do MMC do Gerenciador de Certificados. O **método setSigningCertificate** não obtém o certificado de assinatura, mas informa o Controle de Registro de Cartão Inteligente que obteve anteriormente o certificado de assinatura a ser usado. O **método setSigningCertificate** pesquisa o armazenamento "Meu" do chamador para o certificado de assinatura mais recente correspondente ao modelo de certificado especificado por *bstrCertTemplateName*.

Uma alternativa para **setSigningCertificate** **é ISCrdEnr::setSigningCertificate.**

Depois que um certificado de assinatura é definido, seu nome pode ser recuperado chamando [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr é definido como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
