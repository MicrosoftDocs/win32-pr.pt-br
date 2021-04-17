---
description: O método Close do objeto View encerra a execução da consulta e libera os recursos do banco de dados.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Método View. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770168"
---
# <a name="viewclose-method"></a>Método View. Close

O método **Close** do objeto [**View**](view-object.md) encerra a execução da consulta e libera os recursos do banco de dados.

## <a name="syntax"></a>Sintaxe


```JScript
View.Close()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes que o método [**Execute**](view-execute.md) seja chamado novamente no objeto [**View**](view-object.md) , a menos que todas as linhas do conjunto de resultados tenham sido obtidas com o método [**Fetch**](view-fetch.md) . Ele é chamado internamente quando a exibição é destruída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




