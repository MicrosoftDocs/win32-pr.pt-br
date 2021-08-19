---
description: O método CloseDatabase do objeto Merge fecha o banco de dados Windows Instalador aberto no momento.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Método Merge.CloseDatabase (Mergemod.h)
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
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013024"
---
# <a name="mergeclosedatabase-method"></a>Método Merge.CloseDatabase

O **método CloseDatabase** do objeto [**Merge**](merge-object.md) fecha o banco de dados Windows Instalador aberto no momento.

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

**TRUE** se as alterações devem ser salvas; caso contrário, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Fechar um banco de dados limpa todas as informações de dependência, mas não afeta erros que não foram recuperados.

### <a name="c"></a>C++

Consulte [**Função CloseDatabase.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
