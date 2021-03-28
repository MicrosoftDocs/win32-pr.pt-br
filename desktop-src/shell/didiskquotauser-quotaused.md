---
description: Obtém o uso do disco atual do usuário, em bytes.
title: Propriedade DIDiskQuotaUser. QuotaUsed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090020"
---
# <a name="didiskquotauserquotaused-property"></a>Propriedade DIDiskQuotaUser. QuotaUsed

Obtém o uso do disco atual do usuário, em bytes.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Valor da propriedade

O valor **inteiro** que é definido como a quantidade de espaço em disco em uso no momento. Se a compactação de arquivo NTFS estiver habilitada, **QuotaUsed** refletirá a quantidade de espaço em disco que os dados precisariam em um estado descompactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




