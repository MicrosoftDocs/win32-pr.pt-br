---
description: Obtém o nome do contêiner da conta do usuário.
title: Propriedade DIDiskQuotaUser. AccountContainerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646831"
---
# <a name="didiskquotauseraccountcontainername-property"></a>Propriedade DIDiskQuotaUser. AccountContainerName

Obtém o nome do contêiner da conta do usuário.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Valor da propriedade

Um valor de cadeia de caracteres que é definido como o nome do contêiner da conta do usuário.

## <a name="remarks"></a>Comentários

Para contas sem informações de serviços de diretório, essa propriedade contém o nome de domínio. Para contas com informações de serviços de diretório, essa propriedade contém um nome canônico com o nome do objeto de encerramento removido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




