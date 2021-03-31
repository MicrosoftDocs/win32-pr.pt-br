---
title: Propriedade principal. DisplayName
description: Para scripts, Obtém ou define o nome da entidade de segurança..
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Propriedade DisplayName Agendador de Tarefas
- Propriedade DisplayName Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644743"
---
# <a name="principaldisplayname-property"></a>Propriedade principal. DisplayName

Para scripts, Obtém ou define o nome da entidade de segurança..

## <a name="syntax"></a>Sintaxe


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Valor da propriedade

O nome da entidade de segurança.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o nome de exibição de uma entidade de segurança é especificado no elemento [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) do esquema de Agendador de tarefas.

Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll. Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso. O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso. Por exemplo, definir esse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Beneficiário**](principal.md)
</dt> </dl>

 

 





