---
description: O método ExtractFilesEx do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Método Merge. ExtractFilesEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747963"
---
# <a name="mergeextractfilesex-method"></a>Método Merge. ExtractFilesEx

O método **ExtractFilesEx** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* 
</dt> <dd>

O diretório de destino totalmente qualificado.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

Defina para especificar o uso de nomes de arquivo longos para segmentos de caminho e nomes de arquivo finais.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Esta é uma lista de caminhos totalmente qualificados para os arquivos que foram extraídos com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os arquivos no diretório de destino com o mesmo nome são substituídos. O caminho será criado se ainda não existir.

### <a name="c"></a>C++

Consulte a função [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




