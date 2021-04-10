---
title: RegistrationInfo.DocPropriedade umentation
description: Para scripts, Obtém ou define qualquer documentação adicional para a tarefa.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Agendador de Tarefas de propriedade de documentação
- Propriedade de documentação Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, propriedade de documentação
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085135"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.DocPropriedade umentation

Para scripts, Obtém ou define qualquer documentação adicional para a tarefa.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Valor da propriedade

Qualquer documentação adicional associada à tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, a documentação adicional da tarefa é especificada usando o elemento de [**documentação**](taskschedulerschema-documentation-registrationinfotype-element.md) do esquema de Agendador de tarefas.

Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll. Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso. O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso. Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





