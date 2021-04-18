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
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778726"
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
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




