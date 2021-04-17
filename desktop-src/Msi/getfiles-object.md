---
description: O objeto GetFiles recupera os arquivos necessários em um idioma específico do módulo. Requer que determinadas ações sejam executadas por meio do objeto de mesclagem antes que todas as partes desta interface retornem resultados válidos.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objeto GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748160"
---
# <a name="getfiles-object"></a>Objeto GetFiles

O objeto **GetFiles** recupera os arquivos necessários em um idioma específico do módulo. Requer que determinadas ações sejam executadas por meio do [objeto de mesclagem](merge-object.md) antes que todas as partes desta interface retornem resultados válidos.

## <a name="members"></a>Membros

O objeto **GetFiles** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **GetFiles** tem essas propriedades.



| Propriedade                                               | Descrição                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | A propriedade [**ModuleFiles**](getfiles-modulefiles.md) retorna todas as chaves primárias da [tabela de arquivos](file-table.md) para o módulo aberto no momento.<br/> |



 

## <a name="c"></a>C++

IMsmGetFiles de interface **: IDispatch**

## <a name="interface-id"></a>ID da interface



| Constante              | Valor                                  |
|-----------------------|----------------------------------------|
| **IMsmGetFiles de IID \_** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




