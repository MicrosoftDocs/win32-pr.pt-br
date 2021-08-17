---
description: O objeto Dependency retorna um módulo do qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto dependency (Mergemod.h)
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
ms.openlocfilehash: ac5786dcf3d4818fdfb3f0458cbfa85c923e5200ae69b5cb93d38330c322abf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378884"
---
# <a name="dependency-object"></a>Objeto de dependência

O **objeto Dependency** retorna um módulo do qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.

## <a name="members"></a>Membros

O **objeto Dependency** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Dependency** tem essas propriedades.



| Propriedade                                           | Descrição                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Idioma**](dependency-language.md)<br/> | Retornar o idioma do módulo.<br/>           |
| [**Módulo**](dependency-module.md)<br/>     | Retornar a ID do módulo necessário.<br/> |
| [**Versão**](dependency-version.md)<br/>   | Retornar a versão do módulo necessário.<br/>   |



 

## <a name="c"></a>C++

interface **IMsmDependency: IDispatch**

## <a name="interface-id"></a>Interface ID



| Constante                | Valor                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




