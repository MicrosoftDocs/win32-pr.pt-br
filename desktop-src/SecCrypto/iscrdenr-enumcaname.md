---
description: Enumera o nome das autoridades de certificação (CAs) para um determinado nome de modelo de certificado.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Método ISCrdEnr:: enumCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758163"
---
# <a name="iscrdenrenumcaname-method"></a>Método ISCrdEnr:: enumCAName

O método **enumCAName** enumera o nome das CAS ( [*autoridades de certificação*](../secgloss/c-gly.md) ) para um determinado nome de modelo de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

O índice de base zero para a sequência de enumeração.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação. Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01), o nome se referirá ao nome da máquina da autoridade de certificação. Caso contrário, o nome se refere ao nome da autoridade de certificação.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
