---
description: Recupera o nome da assunto do certificado de assinatura.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: Método ISCrdEnr::getSigningCertificateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622396"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Método ISCrdEnr::getSigningCertificateName

O **método getSigningCertificateName** recupera o nome da assunto do certificado de assinatura.

Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo. Esse método chama a [*função CryptoAPI*](../secgloss/c-gly.md) [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um valor que determina se o certificado é exibido em uma caixa de diálogo. Se esse valor for SCARD ENROLL NO DISPLAY CERT (definido como 0x01), o certificado de assinatura não será exibido; quaisquer outros valores resultarão na exibição do certificado de assinatura na caixa de diálogo \_ \_ \_ \_ Certificado. 

</dd> <dt>

*pbstrSigningCertName* \[ out\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do certificado de assinatura. O certificado de assinatura será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="c"></a>C++

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome do certificado de assinatura. O certificado de assinatura será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Comentários

O **método getSigningCertificateName** retorna o nome da assunto do certificado que você (ou outro administrador) selecionou em uma chamada anterior bem-sucedida para [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) [**ou ISCrdEnr::setSigningCertificate.**](iscrdenr-setsigningcertificate.md) Esse método chama a [**função CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar o nome da assunto de acordo com a sequência descrita para o valor CERT NAME SIMPLE DISPLAY TYPE do parâmetro \_ \_ \_ \_ *dwType* de **CertGetNameString.**

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
