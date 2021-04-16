---
description: 'Recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para ISCrdEnr:: inscrever.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Método ISCrdEnr:: getEnrolledCertificateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758162"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>Método ISCrdEnr:: getEnrolledCertificateName

O método **getEnrolledCertificateName** recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para [**ISCrdEnr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).

Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo. Esse método chama a [](../secgloss/c-gly.md) função CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o certificado é exibido em uma caixa de diálogo. Se esse valor for SCARTAR não \_ registrar \_ nenhum certificado de \_ exibição \_ (definido como 0x01), o certificado registrado não será exibido; qualquer outro valor fará com que o certificado registrado seja exibido na caixa de diálogo **certificado** .

</dd> <dt>

*pBstrCertName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do certificado recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome do certificado recuperado.

## <a name="remarks"></a>Comentários

Como esse método opera em um certificado existente, você deve ter chamado [**ISCrdEnr:: registro**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) com êxito para poder chamar **getEnrolledCertificateName**.

O método **getEnrolledCertificateName** chama a função [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar o nome do certificado de acordo com a sequência descrita para \_ o \_ \_ \_ valor de tipo de exibição simples de nome de certificado do parâmetro *dwType* de **CertGetNameString**.

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

[**ISCrdEnr:: inscrever**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
