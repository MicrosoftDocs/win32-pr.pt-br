---
description: Obtém o uso atual do disco do usuário como uma cadeia de caracteres de texto.
title: Propriedade DIDiskQuotaUser.QuotaUsedText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 40fca179fd415ca548bdb8b07c16696fde54f165bfde7d373087ec1a763e787c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050669"
---
# <a name="didiskquotauserquotausedtext-property"></a>Propriedade DIDiskQuotaUser.QuotaUsedText

Obtém o uso atual do disco do usuário como uma cadeia de caracteres de texto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Valor da propriedade

Um valor de cadeia de caracteres definido como a quantidade de espaço em disco atualmente em uso. Se a compactação de arquivo NTFS estiver habilitada, essa propriedade refletirá a quantidade de espaço em disco que os dados exigiriam em um estado descompactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




