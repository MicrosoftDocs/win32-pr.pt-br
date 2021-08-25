---
description: Especifica o nome do modelo de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: Método ISCrdEnr::setCertTemplateName
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
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993036"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Método ISCrdEnr::setCertTemplateName

O **método setCertTemplateName** especifica o nome do modelo de certificado.

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

*dwFlags* \[ Em\]
</dt> <dd>

Valor que determina se o nome real ou o nome de exibição do modelo de certificado está sendo definido. Se *dwFlags tiver* o valor SCARD ENROLL CERT TEMPLATE DISPLAY NAME, o nome de exibição do modelo de \_ certificado será \_ \_ \_ \_ definido. Caso contrário, o nome real do modelo de certificado será definido.

</dd> <dt>

*bstrCertTemplateName* \[ Em\]
</dt> <dd>

Nome do modelo de certificado que será usado na solicitação de certificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="vb"></a>VB

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

## <a name="remarks"></a>Comentários

Se você não definir o nome do modelo de certificado chamando **ISCrdEnr::setCertTemplateName**, o nome assume como padrão o nome na lista de modelos de certificado disponíveis.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




