---
description: O método ExtractFiles do objeto Merge extrai o arquivo .cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Método Merge.ExtractFiles (Advpub.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926556"
---
# <a name="mergeextractfiles-method"></a>Método Merge.ExtractFiles

O **método ExtractFiles** do objeto [**Merge**](merge-object.md) extrai o arquivo .cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* 
</dt> <dd>

O diretório de destino totalmente qualificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os arquivos no diretório de destino com o mesmo nome são substituídos. O caminho será criado se ele ainda não existir.

**ExtractFiles** sempre extrai arquivos usando nomes de arquivo curtos para o caminho. Para usar nomes de arquivo longos para o caminho, use [**o método ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Consulte [**a função ExtractFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                                     |
| Cabeçalho<br/>  | <dl> <dt>Advpub.h (inclua Mergemod.h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
