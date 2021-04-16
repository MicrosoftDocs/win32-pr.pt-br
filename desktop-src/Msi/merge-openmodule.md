---
description: O método OpenModule do objeto de mesclagem abre um módulo de mesclagem Windows Installer no modo somente leitura. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Método Merge. OpenModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757792"
---
# <a name="mergeopenmodule-method"></a>Método Merge. OpenModule

O método **OpenModule** do objeto de [**mesclagem**](merge-object.md) abre um módulo de mesclagem Windows Installer no modo somente leitura. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nome de arquivo totalmente qualificado apontando para um módulo de mesclagem.

</dd> <dt>

*Idioma* 
</dt> <dd>

Um identificador de idioma válido (LANGid).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função abre o módulo de mesclagem no modo somente leitura e exclui outros programas de gravar no módulo de mesclagem até que o método [**CloseModule**](merge-closemodule.md) seja chamado.

O instalador tenta abrir o módulo no idioma especificado por *idioma* ou em uma linguagem mais geral. Por exemplo, se o *idioma* for especificado como 1033, um módulo com um idioma padrão de 1033, 9 ou 0 pode ser aberto em seu idioma padrão. Um valor de *idioma* 9 abre módulos com um idioma padrão de 9 ou 0. Se o idioma padrão do módulo não atender aos requisitos especificados, será feita uma tentativa de transformar o módulo no idioma solicitado. Se isso falhar, o módulo será transformado em linguagens cada vez mais gerais, até a linguagem neutra. Se nenhuma das transformações for bem-sucedida, o módulo não será aberto. Nesse caso, um erro é adicionado à lista de erros do tipo msmErrorLanguageUnsupported. Se houver um erro ao transformar o módulo no idioma desejado, um erro será adicionado à lista de erros do tipo msmErrorLanguageFailed. Para obter detalhes, consulte a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) . A abertura de um módulo de mesclagem limpa todos os erros que ainda não foram recuperados.

### <a name="c"></a>C++

Consulte a função [**AbrirMódulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
