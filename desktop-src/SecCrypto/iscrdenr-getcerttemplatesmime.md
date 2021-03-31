---
description: Usado para determinar se um modelo de certificado contém o \_ uso da chave de proteção de email szOID PKIX \_ KP \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Método ISCrdEnr:: getCertTemplateSMIME'
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
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829529"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Método ISCrdEnr:: getCertTemplateSMIME

O método **getCertTemplateSMIME** é usado para determinar se um modelo de certificado contém o \_ uso da chave de proteção de email szOID PKIX \_ KP \_ \_ .

Se esse uso de chave fizer parte do modelo de certificado, o modelo de certificado dará suporte a operações de S/MIME ( [*Internet Mail Extensions) seguras/multipropósitos*](../secgloss/s-gly.md) .

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

*bstrCertTemplateName* \[ no\]
</dt> <dd>

O nome do certificado que está sendo consultado para o uso da chave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ fora\]
</dt> <dd>

Um ponteiro para um **DWORD** que retorna um valor de um se *bstrCertTemplateName* dá suporte a S/MIME; caso contrário, ele retornará zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Valor **longo** de um se *bstrCertTemplateName* dá suporte a S/MIME; caso contrário, zero.

## <a name="remarks"></a>Comentários

A constante para szOID \_ PKIX \_ KP \_ email \_ Protection é definida em Wincrypt. h.

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

 

 
