---
description: Especifica o nome do modelo de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Método ISCrdEnr:: setCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758011"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Método ISCrdEnr:: setCertTemplateName

O método **setCertTemplateName** especifica o nome do modelo de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Valor que determina se o nome real ou o nome de exibição do modelo de certificado está sendo definido. Se *dwFlags* tiver o valor scartar \_ registrar \_ o \_ \_ \_ nome de exibição do modelo de certificado, o nome de exibição do modelo será definido. Caso contrário, o nome real do modelo de certificado será definido.

</dd> <dt>

*bstrCertTemplateName* \[ no\]
</dt> <dd>

Nome do modelo de certificado que será usado na solicitação de certificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Se você não definir o nome do modelo de certificado chamando **ISCrdEnr:: setCertTemplateName**, o nome será padronizado como o nome na lista de modelos de certificado disponíveis.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




