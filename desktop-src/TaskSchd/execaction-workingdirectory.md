---
title: Propriedade ExecAction.WorkingDirectory
description: Para scripts, obtém ou define o diretório que contém o arquivo executável ou os arquivos usados pelo arquivo executável.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Propriedade WorkingDirectory Agendador de Tarefas
- Propriedade WorkingDirectory Agendador de Tarefas objeto , ExecAction
- Objeto ExecAction Agendador de Tarefas propriedade , WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139439"
---
# <a name="execactionworkingdirectory-property"></a>Propriedade ExecAction.WorkingDirectory

Para scripts, obtém ou define o diretório que contém o arquivo executável ou os arquivos usados pelo arquivo executável.

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valor da propriedade

O diretório que contém o arquivo executável ou os arquivos usados pelo arquivo executável.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML, o diretório de trabalho do aplicativo é especificado no elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) do Agendador de Tarefas esquema.

O caminho é verificado para verificar se ele é válido quando a tarefa é registrada, não quando essa propriedade está definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





