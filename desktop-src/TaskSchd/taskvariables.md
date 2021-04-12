---
title: Objeto TaskVariables
description: Objeto de script que define as variáveis de tarefa que podem ser passadas como parâmetros para manipuladores de tarefas e executáveis externos que são iniciados por tarefas.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Agendador de Tarefas de objeto TaskVariables
- Agendador de Tarefas de objeto TaskVariables, descrito
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455691"
---
# <a name="taskvariables-object"></a>Objeto TaskVariables

Objeto de script que define as variáveis de tarefa que podem ser passadas como parâmetros para manipuladores de tarefas e executáveis externos que são iniciados por tarefas.

## <a name="members"></a>Membros

O objeto **TaskVariables** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **TaskVariables** tem esses métodos.



| Método                                         | Descrição                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Usado para compartilhar o contexto entre etapas e tarefas diferentes que estão na mesma instância de trabalho.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Obtém as variáveis de entrada para uma tarefa.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Define as variáveis de saída para uma tarefa.<br/>                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





