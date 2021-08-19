---
description: Enumera os nomes de modelo de certificado.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: Método ISCrdEnr::enumCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: aab979e77e9e3e61b9d35125accbdf01934764d5a09daf161480646cdec28e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005194"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Método ISCrdEnr::enumCertTemplateName

O **método enumCertTemplateName** enumera os nomes de modelo de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

O índice baseado em zero para a sequência de enumeração.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um valor que determina se o modelo de certificado enumerado se aplica a certificados de usuário ou computador. Se esse valor for SCARD ENROLL USER CERT TEMPLATE (definido como \_ \_ 1), a \_ \_ enumeração se aplicará aos modelos de certificado do usuário. Se esse valor for SCARD ENROLL MACHINE CERT TEMPLATE (definido como \_ \_ 2), a \_ \_ enumeração se aplicará aos modelos de certificado do computador.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do modelo de certificado enumerado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="c"></a>C++

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

### <a name="vb"></a>VB

Uma cadeia de caracteres que contém o nome do modelo de certificado enumerado.

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

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




