---
description: Usado para determinar se um modelo de certificado contém o uso da chave SZOID \_ PKIX \_ KP \_ EMAIL \_ PROTECTION.
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: Método ISCrdEnr::getCertTemplateSMIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515956"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Método ISCrdEnr::getCertTemplateSMIME

O **método getCertTemplateSMIME** é usado para determinar se um modelo de certificado contém o uso da chave SzOID \_ \_ PKIX KP EMAIL \_ \_ PROTECTION.

Se esse uso de chave faz parte do modelo de certificado, o modelo de certificado dá suporte a operações S/MIME (Extensões de [*Internet Mail Seguras/Multipropósitos).*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrCertTemplateName* \[ Em\]
</dt> <dd>

O nome do certificado que está sendo consultado para o uso da chave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ out\]
</dt> <dd>

Um ponteiro para um **DWORD que** retornará um valor de um se *bstrCertTemplateName* for compatível com S/MIME; caso contrário, retornará zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="c"></a>C++

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

### <a name="vb"></a>VB

**Valor** longo de um se *bstrCertTemplateName for* compatível com S/MIME; caso contrário, zero.

## <a name="remarks"></a>Comentários

A constante para szOID \_ PKIX \_ KP \_ EMAIL PROTECTION é definida \_ em Wincrypt.h.

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

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
