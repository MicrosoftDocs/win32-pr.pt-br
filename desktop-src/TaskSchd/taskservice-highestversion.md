---
title: Propriedade TaskService. HighestVersion
description: Para scripts, indica a versão mais recente do Agendador de Tarefas a que um computador dá suporte.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Agendador de Tarefas da propriedade HighestVersion
- Propriedade HighestVersion Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, Propriedade HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645208"
---
# <a name="taskservicehighestversion-property"></a>Propriedade TaskService. HighestVersion

Para scripts, indica a versão mais recente do Agendador de Tarefas a que um computador dá suporte.

## <a name="syntax"></a>Syntax


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valor da propriedade

A versão mais recente do Agendador de Tarefas a que um computador dá suporte. A versão mais alta é um valor que é dividido em MajorVersion/MinorVersion no limite de 16 bits. O serviço de Agendador de Tarefas retorna 1 para a versão principal e 2 para a versão secundária. Use a função [CLng](/previous-versions//ck4c5842(v=vs.85)) para obter o valor inteiro da propriedade.

## <a name="examples"></a>Exemplos

O código a seguir mostra como usar a função [CLng](/previous-versions//ck4c5842(v=vs.85)) para obter o valor da propriedade **HighestVersion** .


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

