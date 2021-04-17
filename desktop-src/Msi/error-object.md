---
description: O objeto Error Retorna as informações de um único erro de mesclagem.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objeto de erro (Mergemod. h)
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
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747981"
---
# <a name="error-object"></a>Objeto de erro

O objeto **Error** retorna as informações de um único erro de mesclagem.

## <a name="members"></a>Membros

O objeto de **erro** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **erro** tem essas propriedades.



| Propriedade                                                | Descrição                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Retorna as chaves primárias da linha na tabela de banco de dados que causou o erro.<br/> |
| [**Banco de dados**](error-databasetable.md)<br/> | Retorna o nome da tabela do banco de dados que está causando o erro.<br/>           |
| [**Idioma**](error-language.md)<br/>           | Retorne o idioma do erro.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Retorna as chaves primárias da linha na tabela de módulo que causou o erro.<br/>   |
| [**Módulotable**](error-moduletable.md)<br/>     | Retorna o nome da tabela do módulo que está causando o erro.<br/>             |
| [**Caminho**](error-path.md)<br/>                   | Retorne o caminho para o arquivo ou diretório causando o erro. Atualmente não utilizado.<br/>    |
| [**Tipo**](error-type.md)<br/>                   | Retornar o tipo de erro.<br/>                                                        |



 

## <a name="c"></a>C++

IMsmError de interface **: IDispatch**

## <a name="interface-id"></a>ID da interface



| Constante           | Valor                                  |
|--------------------|----------------------------------------|
| **IMsmError de IID \_** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




