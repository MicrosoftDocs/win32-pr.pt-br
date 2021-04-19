---
description: A propriedade Environment do objeto instalador é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Propriedade Installer. Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747544"
---
# <a name="installerenvironment-property"></a>Propriedade Installer. Environment

A propriedade **Environment** do objeto [**instalador**](installer-object.md) é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valor da propriedade

O nome da variável de ambiente a ser lida ou gravada. Isso não diferencia maiúsculas de minúsculas.

## <a name="remarks"></a>Comentários

Definir uma variável de ambiente com a propriedade de **ambiente** afeta apenas a sessão ativa. Para fazer alterações persistentes em uma variável de ambiente, use a [tabela de ambiente](environment-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




