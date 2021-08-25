---
description: A propriedade DatabaseState do objeto Database é uma propriedade somente leitura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propriedade Database.DatabaseState
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
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745636"
---
# <a name="databasedatabasestate-property"></a>Propriedade Database.DatabaseState

A **propriedade DatabaseState** do objeto [**Database**](database-object.md) é uma propriedade somente leitura.

Essa propriedade retorna o estado de persistência do banco de dados como um dos parâmetros a seguir.



| Estado do banco de dados        | Valor | Descrição                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | O banco de dados é aberto como somente leitura. As alterações em dados persistentes não são permitidas e os dados temporários não são salvos. |
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
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase é definido como \_ 000C109D-0000-0000-C000-00000000046<br/>                                                                                                                                                                            |



 

 




