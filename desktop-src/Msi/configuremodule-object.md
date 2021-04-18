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
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751446"
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
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




