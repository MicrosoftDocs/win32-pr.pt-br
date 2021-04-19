---
description: O método Connect do objeto de mesclagem conecta um módulo a um recurso adicional. O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados. O recurso deve existir antes de chamar essa função.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Método Merge. Connect (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757120"
---
# <a name="mergeconnect-method"></a>Método Merge. Connect

O método **Connect** do objeto de [**mesclagem**](merge-object.md) conecta um módulo a um recurso adicional. O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados. O recurso deve existir antes de chamar essa função.

As alterações feitas no banco de dados não são salvas no disco, a menos que o método [**CloseDatabase**](merge-closedatabase.md) seja chamado com *BCommit* definido como **true**.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recurso* 
</dt> <dd>

O nome de um recurso já existente no banco de dados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os erros podem ser recuperados por meio da propriedade [**Errors**](merge-errors.md) . Erros e mensagens informativas são postados no arquivo de log atual.

### <a name="c"></a>C++

Consulte [**conectar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
