---
description: O objeto Error retorna as informações de um único erro de mesclagem.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objeto de erro (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947027"
---
# <a name="error-object"></a>Objeto de erro

O **objeto Error** retorna as informações de um único erro de mesclagem.

## <a name="members"></a>Membros

O **objeto Error** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Error** tem essas propriedades.



| Propriedade                                                | Descrição                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Retorna as chaves primárias da linha na tabela de banco de dados que causou o erro.<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | Retorna o nome da tabela no banco de dados que está causando o erro.<br/>           |
| [**Idioma**](error-language.md)<br/>           | Retornar o idioma do erro.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Retorna as chaves primárias da linha na tabela do módulo que causou o erro.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Retorna o nome da tabela no módulo que está causando o erro.<br/>             |
| [**Caminho**](error-path.md)<br/>                   | Retorne o caminho para o arquivo ou diretório que está causando o erro. Atualmente não éusado.<br/>    |
| [**Tipo**](error-type.md)<br/>                   | Retornar o tipo de erro.<br/>                                                        |



 

## <a name="c"></a>C++

interface **IMsmError: IDispatch**

## <a name="interface-id"></a>Interface ID



| Constante           | Valor                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




