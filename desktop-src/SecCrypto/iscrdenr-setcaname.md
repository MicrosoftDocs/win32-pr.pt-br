---
description: Especifica o nome da autoridade de certificação (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Método ISCrdEnr:: setCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756856"
---
# <a name="iscrdenrsetcaname-method"></a>Método ISCrdEnr:: setCAName

O método **setCAName** especifica o nome da [*autoridade de certificação*](../secgloss/c-gly.md) (CA).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Valor que especifica se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação. Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01), o nome se referirá ao nome da máquina da autoridade de certificação. Caso contrário, o nome se refere ao nome da autoridade de certificação.

</dd> <dt>

*bstrCertTemplateName* \[ no\]
</dt> <dd>

Nome do modelo de certificado.

</dd> <dt>

*bstrCAName* \[ no\]
</dt> <dd>

Nome da autoridade de certificação a ser usado com o modelo de certificado especificado por *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="vb"></a>VB

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Use esse método para especificar uma autoridade de certificação para um modelo de certificado.

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

 

 
