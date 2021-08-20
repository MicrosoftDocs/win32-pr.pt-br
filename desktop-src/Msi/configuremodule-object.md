---
description: O objeto ConfigureModule é uma interface implementada pelo cliente.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objeto ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143705"
---
# <a name="configuremodule-object"></a>Objeto ConfigureModule

O **objeto ConfigureModule** é uma interface implementada pelo cliente. Mergemod.dllchama métodos na interface **IMsmConfigureModule** para solicitar que a ferramenta cliente forneça informações de configuração. O módulo é configurado com base nas respostas do cliente a chamadas nesta interface.

## <a name="members"></a>Membros

O objeto **ConfigureModule** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **ConfigureModule** tem esses métodos.



| Método                                                           | Descrição                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Chamado por Mergemod.dll para obter números inteiros usados para configurar o módulo.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Chamado por Mergemod.dll para obter o texto usado para configurar o módulo.<br/>     |



 

## <a name="remarks"></a>Comentários

### <a name="c"></a>C++

IMsmConfigureModule de interface **: IDispatch**

### <a name="interface-id"></a>ID da interface



| Constante                     | Valor                                  |
|------------------------------|----------------------------------------|
| **IMsmConfigureModule de IID \_** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




