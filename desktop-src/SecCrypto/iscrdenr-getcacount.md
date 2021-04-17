---
description: Retorna o número de autoridades de certificação (CAs) que desejam emitir um certificado com base no modelo de certificado especificado.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Método ISCrdEnr:: getCACount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780468"
---
# <a name="iscrdenrgetcacount-method"></a>Método ISCrdEnr:: getCACount

O método **getCACount** retorna o número de [*autoridades de certificação*](../secgloss/c-gly.md) (CAS) que desejam emitir um certificado com base no modelo de certificado especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrCertTemplateName* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que representa o nome do modelo de certificado.

</dd> <dt>

*pdwCACount* \[ fora\]
</dt> <dd>

Um ponteiro para um **longo** que retorna o número de CAS disponíveis que emitirão um certificado para o modelo de certificado especificado em *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Um valor **longo** que representa o número de CAS disponíveis que emitirão um certificado para o modelo de certificado especificado em *bstrCertTemplateName*.

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

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
