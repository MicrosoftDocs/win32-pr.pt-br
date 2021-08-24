---
description: O método CreateSourceImage do objeto Merge permite que o cliente Extraia os arquivos de um módulo para uma imagem de origem no disco após uma mesclagem, levando em conta as alterações ao módulo que podem ter sido feitas durante a configuração do módulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Método Merge. CreateSourceImage (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3e50fca7adaeced7f6f2130aeb86cf1ee74db18ae505575c8ce37b1bb85a4010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926636"
---
# <a name="mergecreatesourceimage-method"></a>Método Merge. CreateSourceImage

O método **CreateSourceImage** do objeto [**Merge**](merge-object.md) permite que o cliente Extraia os arquivos de um módulo para uma imagem de origem no disco após uma mesclagem, levando em conta as alterações ao módulo que podem ter sido feitas durante a configuração do módulo. A lista de arquivos a serem extraídos é obtida da tabela de arquivos do módulo durante o processo de mesclagem. A lista de arquivos consiste em cada arquivo copiado com êxito da tabela de arquivos do módulo para o banco de dados de destino. As entradas de tabela de arquivo que não foram copiadas devido a conflitos de chave primária com linhas existentes no banco de dados não fazem parte dessa lista. No momento da criação da imagem, o diretório de cada um desses arquivos é proveniente do banco de dados aberto (post-Merge). O caminho especificado no parâmetro *path* é a raiz da imagem de origem para a instalação. *fLongFileNames* determina se nomes de arquivo longos são ou não usados para segmentos de caminho e nomes de arquivo finais. A função falhará se nenhum banco de dados estiver aberto, nenhum módulo estiver aberto ou nenhuma mesclagem tiver sido executada.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* 
</dt> <dd>

O caminho da raiz da imagem de origem para a instalação.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames* determina se nomes de arquivo longos são ou não usados para segmentos de caminho e nomes de arquivo finais.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Esta é uma lista de caminhos totalmente qualificados para os arquivos que foram extraídos com êxito.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os arquivos no diretório de destino com o mesmo nome são substituídos. O caminho será criado se ainda não existir.

### <a name="c"></a>C++

Consulte a função [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




