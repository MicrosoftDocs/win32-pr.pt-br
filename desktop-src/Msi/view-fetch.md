---
description: O método FETCH do objeto View recupera a próxima linha de dados da coluna se houver mais linhas disponíveis no conjunto de resultados; caso contrário, será NULL. Chame o método execute antes do método Fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: Método View. Fetch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758609"
---
# <a name="viewfetch-method"></a>Método View. Fetch

O método **Fetch** do objeto [**View**](view-object.md) recupera a próxima linha de dados da coluna se houver mais linhas disponíveis no conjunto de resultados; caso contrário, será NULL. Chame o método [**Execute**](view-execute.md) antes do método **Fetch** .

## <a name="syntax"></a>Sintaxe


```JScript
View.Fetch()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O mesmo objeto de [**registro**](record-object.md) deve ser usado para recuperar os dados em várias linhas, caso contrário, o objeto deve ser liberado saindo do escopo. O registro pode ser testado para o final do conjunto de resultados usando a sintaxe "If FetchRecord Is Nothing".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




