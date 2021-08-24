---
description: Recupera o nome da AC (autoridade de certificação) especificada para um determinado modelo de certificado.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: Método ISCrdEnr::getCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 6de5d1108ab09c9658af307d6a67c5a94a5dc35514720a221540de263f516c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960276"
---
# <a name="iscrdenrgetcaname-method"></a>Método ISCrdEnr::getCAName

O **método getCAName** recupera o nome da AC [*(autoridade*](../secgloss/c-gly.md) de certificação) especificada para um determinado modelo de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um valor que determina se o nome se refere ao nome da AC ou ao nome do computador da AC. Se esse valor for SCARD ENROLL CA MACHINE NAME (definido como 0x01), o nome se referirá ao nome do computador da AC; caso contrário, o nome se referirá ao nome \_ \_ da \_ \_ AC.

</dd> <dt>

*bstrCertTemplateName* \[ Em\]
</dt> <dd>

O nome do modelo de certificado.

</dd> <dt>

*pbstrCAName* \[ out\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome da AC.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="c"></a>C++

Se o método for bem-sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome da AC.

## <a name="remarks"></a>Comentários

O nome da AC padrão é o primeiro nome na lista de CAs disponíveis.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
