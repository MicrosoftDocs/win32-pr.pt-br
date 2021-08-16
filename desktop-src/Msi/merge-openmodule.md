---
description: O método OpenModule do objeto Merge abre Windows módulo de mesclagem do instalador no modo somente leitura. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Método Merge.OpenModule (Mergemod.h)
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
ms.openlocfilehash: 4659fbd2c96d883b04e653fc67c6aa3017f16135405f956bf9b4eb78101bb404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628722"
---
# <a name="mergeopenmodule-method"></a>Método Merge.OpenModule

O **método OpenModule** do objeto [**Merge**](merge-object.md) abre Windows módulo de mesclagem do instalador no modo somente leitura. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.

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

Um LANGID (identificador de idioma) válido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função abre o módulo de mesclagem no modo somente leitura e exclui outros programas de escrever no módulo de mesclagem até que [**o método CloseModule**](merge-closemodule.md) seja chamado.

O instalador tenta abrir o módulo no idioma especificado por *Language* ou um idioma mais geral. Por exemplo, se *Language* for especificado como 1033, um módulo com um idioma padrão 1033, 9 ou 0 poderá ser aberto em seu idioma padrão. Um *valor* de Idioma de 9 abre módulos com um idioma padrão de 9 ou 0. Se o idioma padrão do módulo não atender aos requisitos especificados, será feita uma tentativa de transformar o módulo no idioma solicitado. Se isso falhar, o módulo será transformado em idiomas cada vez mais gerais, até o idioma neutro. Se nenhuma das transformaçãos for bem-sucedida, o módulo não será aberto. Nesse caso, um erro é adicionado à lista de erros do tipo msmErrorLanguageUnsupported. Se houver um erro ao transformar o módulo no idioma desejado, um erro será adicionado à lista de erros do tipo msmErrorLanguageFailed. Para obter detalhes, consulte [**a propriedade Type**](error-type.md) do objeto [**Error.**](error-object.md) Abrir um módulo de mesclagem limpa todos os erros que ainda não foram recuperados.

### <a name="c"></a>C++

Consulte [**Função OpenModule.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
