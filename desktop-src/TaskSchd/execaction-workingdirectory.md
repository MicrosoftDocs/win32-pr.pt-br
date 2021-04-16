---
title: Propriedade execaction. WorkingDirectory
description: Para scripts, Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Agendador de Tarefas da propriedade WorkingDirectory
- Propriedade WorkingDirectory Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, Propriedade WorkingDirectory
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
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758392"
---
# <a name="execactionworkingdirectory-property"></a>Propriedade execaction. WorkingDirectory

Para scripts, Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valor da propriedade

O diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, o diretório de trabalho do aplicativo é especificado no elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) do esquema de Agendador de tarefas.

O caminho é verificado para certificar-se de que ele é válido quando a tarefa é registrada, não quando essa propriedade é definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





