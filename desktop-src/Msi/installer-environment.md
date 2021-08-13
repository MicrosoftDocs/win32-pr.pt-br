---
description: A propriedade Environment do objeto Installer é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Propriedade Installer.Environment
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
ms.openlocfilehash: 8f24237da6c140ef0d38ff17591bf214698cfa6731bd4e8d3cfcaa613b335404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631682"
---
# <a name="installerenvironment-property"></a>Propriedade Installer.Environment

A **propriedade Environment** do objeto [**Installer**](installer-object.md) é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valor da propriedade

O nome da variável de ambiente a ser lida ou escrita. Isso não faz sentido para maiúsculas de minúsculas.

## <a name="remarks"></a>Comentários

Definir uma variável de ambiente com **a propriedade** Ambiente afeta apenas a sessão ativa. Para fazer alterações persistentes em uma variável de ambiente, use [a tabela Ambiente](environment-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




