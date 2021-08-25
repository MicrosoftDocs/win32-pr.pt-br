---
title: Propriedade RegistrationInfo.Description
description: Para scripts, obtém ou define a descrição da tarefa.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Propriedade description Agendador de Tarefas
- Propriedade Description Agendador de Tarefas objeto , RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas propriedade , Descrição
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872456"
---
# <a name="registrationinfodescription-property"></a>Propriedade RegistrationInfo.Description

Para scripts, obtém ou define a descrição da tarefa.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Valor da propriedade

A descrição da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, a descrição da tarefa é especificada usando o elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) do esquema Agendador de Tarefas.

Ao definir esse valor de propriedade, o valor pode ser texto recuperado de um arquivo de .dll recurso. Uma cadeia de caracteres especializada é usada para referenciar o texto do arquivo de recurso. O formato da cadeia de caracteres é $(@ Dll , ResourceID ) em que Dll é o caminho para o arquivo .dll que contém o recurso e ResourceID é o identificador do texto \[ \] do \[ \] \[ \] \[ \] recurso. Por exemplo, a definição desse valor da propriedade como $(@ %SystemRoot% System32ResourceName.dll, -101) definirá a propriedade como o valor do texto do recurso com um identificador igual \\ \\ a -101 no arquivo %SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





