---
description: A propriedade DatabaseState do objeto de banco de dados é uma propriedade somente leitura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propriedade Database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747555"
---
# <a name="databasedatabasestate-property"></a>Propriedade Database. DatabaseState

A propriedade **DatabaseState** do objeto de [**banco de dados**](database-object.md) é uma propriedade somente leitura.

Essa propriedade retorna o estado de persistência do banco de dados como um dos parâmetros a seguir.



| Estado do banco de dados        | Valor | Descrição                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | O banco de dados é aberto como somente leitura. As alterações nos dados persistentes não são permitidas e os dados temporários não são salvos. |
| msiDatabaseStateWrite | 1     | O banco de dados está totalmente operacional para leitura e gravação.                                                          |



 

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




