---
description: Recupera o nome da autoridade de certificação (CA) especificada para um determinado modelo de certificado.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Método ISCrdEnr:: getCAName'
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
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171485"
---
# <a name="iscrdenrgetcaname-method"></a>Método ISCrdEnr:: getCAName

O método **getCAName** recupera o nome da autoridade de [*certificação*](../secgloss/c-gly.md) (CA) especificada para um determinado modelo de certificado.

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

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação. Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01) e o nome se referirá ao nome da máquina da autoridade de certificação; caso contrário, o nome se referirá ao nome da autoridade de certificação.

</dd> <dt>

*bstrCertTemplateName* \[ no\]
</dt> <dd>

O nome do modelo de certificado.

</dd> <dt>

*pbstrCAName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que retorna o nome da autoridade de certificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Uma cadeia de caracteres que representa o nome da autoridade de certificação.

## <a name="remarks"></a>Comentários

O nome da autoridade de certificação padrão é o nome da lista de CAs disponível.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
