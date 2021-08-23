---
description: Define ou Obtém o limite de aviso do usuário, em bytes.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Propriedade DIDiskQuotaUser. QuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 38caa5ef5ded6ed40708314c6063fba13a74cbbe506465aed55e8504898a9307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032784"
---
# <a name="didiskquotauserquotathreshold-property"></a>Propriedade DIDiskQuotaUser. QuotaThreshold

Define ou Obtém o limite de aviso do usuário, em bytes.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>Valor da propriedade

Um valor **inteiro** que especifica ou recebe o limite de aviso do usuário. Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




