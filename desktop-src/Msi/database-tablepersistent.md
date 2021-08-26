---
description: A propriedade TablePersistent do objeto Database retorna o estado de persistência da tabela como um dos parâmetros a seguir.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propriedade Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5eaf32996adef39976ba9fbaf88834c339e27dbe13c4e7fbcd1928ac1973b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129636"
---
# <a name="databasetablepersistent-property"></a>Propriedade Database. TablePersistent

A propriedade **TablePersistent** do objeto [**Database**](database-object.md) retorna o estado de persistência da tabela como um dos parâmetros a seguir.



| Estado da tabela               | Valor | Descrição                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | A tabela é temporária.            |
| msiEvaluateConditionTrue  | 1     | A tabela é persistente.           |
| msiEvaluateConditionNone  | 2     | A tabela não está no banco de dados.  |
| msiEvaluateConditionError | 3     | Nome de tabela inválido ou ausente. |



 

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




