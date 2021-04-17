---
description: A propriedade ModuleFiles do objeto GetFiles retorna todas as chaves primárias da tabela de arquivos para o módulo aberto no momento.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Propriedade GetFiles. ModuleFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811846"
---
# <a name="getfilesmodulefiles-property"></a>Propriedade GetFiles. ModuleFiles

A propriedade **ModuleFiles** do objeto [**GetFiles**](getfiles-object.md) retorna todas as chaves primárias da [tabela de arquivos](file-table.md) para o módulo aberto no momento. As chaves primárias são retornadas como uma coleção de cadeias de caracteres. O módulo deve ser aberto por uma chamada para o método [**OpenModule**](merge-openmodule.md) do [objeto de mesclagem](merge-object.md) antes de chamar **ModuleFiles**.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Observe que a ordem dos arquivos listados na coleção pode não estar na mesma sequência, conforme listado na tabela de arquivos.

Se o módulo não tiver nenhuma tabela de arquivos ou não contiver nenhum arquivo no idioma específico, ModuleFiles retornará uma coleção vazia de cadeias de caracteres.

### <a name="c"></a>C++

Consulte [**obter \_**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) a função ModuleFiles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
