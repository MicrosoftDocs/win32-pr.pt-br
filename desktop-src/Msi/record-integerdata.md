---
description: Essa é a propriedade IntegerData do objeto Record. Essa propriedade de leitura/gravação transfere dados inteiros de 32 bits para dentro ou para fora de um campo especificado no registro. Se um valor de campo não puder ser convertido em um inteiro, msiDatabaseNullInteger será retornado.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Propriedade Record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748572"
---
# <a name="recordintegerdata-property"></a>Propriedade Record. IntegerData

Essa é a propriedade **IntegerData** do objeto [**Record**](record-object.md) . Essa propriedade de leitura/gravação transfere dados inteiros de 32 bits para dentro ou para fora de um campo especificado no registro. Se um valor de campo não puder ser convertido em um inteiro, msiDatabaseNullInteger será retornado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Campo obrigatório número do valor dentro do registro, baseado em 1.

## <a name="remarks"></a>Comentários

Para definir um campo de inteiro de registro como nulo, use msiDatabaseNullInteger. O valor retornado de um campo inexistente é msiDatabaseNullInteger. A tentativa de armazenar um valor em um campo inexistente causa um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




