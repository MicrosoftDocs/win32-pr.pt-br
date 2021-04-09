---
description: Recupera o nome do modelo de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Método ISCrdEnr:: getCertTemplateName'
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
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171483"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Método ISCrdEnr:: getCertTemplateName

O método **getCertTemplateName** recupera o nome do modelo de certificado.

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

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o nome real ou o nome de exibição do modelo de certificado é retornado. Se *dwFlags* tiver o valor scartar \_ registrar \_ o \_ \_ nome de exibição do modelo de certificado \_ , o nome de exibição do modelo de certificados será recuperado; caso contrário, o nome real do modelo de certificado será exibido.

</dd> <dt>

*pbstrCertTemplateName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome do modelo de certificado que será usado na [*solicitação de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome do modelo de certificado que será usado na [*solicitação de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Comentários

Se você não definir o nome do modelo de certificado chamando [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), o nome será padronizado como o nome na lista de modelos de certificado disponíveis.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
