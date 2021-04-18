---
description: Recupera o nome da entidade do certificado de autenticação.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Método ISCrdEnr:: getSigningCertificateName'
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
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370737"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Método ISCrdEnr:: getSigningCertificateName

O método **getSigningCertificateName** recupera o nome da entidade do certificado de autenticação.

Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo. Esse método chama a [](../secgloss/c-gly.md) função CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

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

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o certificado é exibido em uma caixa de diálogo. Se esse valor for SCARTAR \_ não \_ registrar \_ nenhum \_ certificado de exibição (definido como 0x01), o certificado de autenticação não será exibido; todos os outros valores resultarão na exibição do certificado de autenticação na caixa de diálogo **certificado** .

</dd> <dt>

*pbstrSigningCertName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do certificado de autenticação. O certificado de autenticação será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome do certificado de autenticação. O certificado de autenticação será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Comentários

O método **getSigningCertificateName** retorna o nome da entidade do certificado que você (ou outro administrador) selecionou em uma chamada bem-sucedida anterior para [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) ou [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md). Esse método chama a função [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar o nome da entidade de acordo com a sequência descrita para \_ o \_ \_ \_ valor de tipo de exibição simples do nome do certificado do parâmetro *dwType* do **CertGetNameString**.

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
