---
description: O método ExtractFiles do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Método Merge. ExtractFiles (Advpub. h)
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
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783269"
---
# <a name="mergeextractfiles-method"></a>Método Merge. ExtractFiles

O método **ExtractFiles** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.

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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os arquivos no diretório de destino com o mesmo nome são substituídos. O caminho será criado se ainda não existir.

O **ExtractFiles** sempre extrai arquivos usando nomes de arquivo curtos para o caminho. Para usar nomes de arquivo longos para o caminho, use o [**método ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Consulte a função [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                                     |
| parâmetro<br/>  | <dl> <dt>Advpub. h (incluir Mergemod. h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
