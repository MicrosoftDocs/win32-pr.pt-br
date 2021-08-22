---
description: Recupera o nome do modelo de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: Método ISCrdEnr::getCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: aaf37f3907bc2b26ca1adbbded7be5ed7897a74ea9664d4353354d5ad9657d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409616"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Método ISCrdEnr::getCertTemplateName

O **método getCertTemplateName** recupera o nome do modelo de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um valor que determina se o nome real ou o nome de exibição do modelo de certificado é retornado. Se *dwFlags* tiver o valor SCARD ENROLL CERT TEMPLATE DISPLAY NAME, o nome de exibição do modelo de certificado será recuperado; caso contrário, o nome real do modelo de certificado \_ \_ será \_ \_ \_ exibido.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do modelo de certificado que será usado na solicitação [*de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="c"></a>C++

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome do modelo de certificado que será usado na [*solicitação de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Comentários

Se você não definir o nome do modelo de certificado chamando [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), o nome assume como padrão o nome na lista de modelos de certificado disponíveis.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
