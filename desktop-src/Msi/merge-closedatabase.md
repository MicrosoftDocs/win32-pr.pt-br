---
description: O método CloseDatabase do objeto de mesclagem fecha o banco de dados Windows Installer aberto no momento.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Método Merge. CloseDatabase (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757793"
---
# <a name="mergeclosedatabase-method"></a>Método Merge. CloseDatabase

O método **CloseDatabase** do objeto de [**mesclagem**](merge-object.md) fecha o banco de dados Windows Installer aberto no momento.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCommit* 
</dt> <dd>

**True** se as alterações devem ser salvas; caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Fechar um banco de dados limpa todas as informações de dependência, mas não afeta os erros que não foram recuperados.

### <a name="c"></a>C++

Consulte a função [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
