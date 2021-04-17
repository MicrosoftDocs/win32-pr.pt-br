---
description: O objeto Dependency retorna um módulo no qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto Dependency (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749591"
---
# <a name="dependency-object"></a>Objeto de dependência

O objeto **Dependency** retorna um módulo no qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.

## <a name="members"></a>Membros

O objeto de **dependência** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **dependência** tem essas propriedades.



| Propriedade                                           | Descrição                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Idioma**](dependency-language.md)<br/> | Retorne o idioma do módulo.<br/>           |
| [**Módulo**](dependency-module.md)<br/>     | Retornar a ID do módulo necessário.<br/> |
| [**Versão**](dependency-version.md)<br/>   | Retorne a versão do módulo necessário.<br/>   |



 

## <a name="c"></a>C++

IMsmDependency de interface **: IDispatch**

## <a name="interface-id"></a>ID da interface



| Constante                | Valor                                  |
|-------------------------|----------------------------------------|
| **IMsmDependency de IID \_** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




