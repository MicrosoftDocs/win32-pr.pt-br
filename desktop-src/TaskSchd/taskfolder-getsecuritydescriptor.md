---
title: Propriedade TaskFolder.GetSecurityDescriptor
description: Para scripts, obtém o descritor de segurança para a pasta.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Propriedade GetSecurityDescriptor Agendador de Tarefas
- Propriedade GetSecurityDescriptor Agendador de Tarefas objeto , TaskFolder
- Objeto TaskFolder Agendador de Tarefas , propriedade GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851565299b7e6d1c29e2e53d87fb27aa30297921cc194f3cce753fc8d22a6bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080316"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>Propriedade TaskFolder.GetSecurityDescriptor

Para scripts, obtém o descritor de segurança para a pasta.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





