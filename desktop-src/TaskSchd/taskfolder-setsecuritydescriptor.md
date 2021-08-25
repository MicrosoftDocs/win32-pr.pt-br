---
title: Propriedade TaskFolder. SetSecurityDescriptor
description: Para scripts, define o descritor de segurança para a pasta.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Agendador de Tarefas da propriedade SetSecurityDescriptor
- Propriedade SetSecurityDescriptor Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033786"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Propriedade TaskFolder. SetSecurityDescriptor

Para scripts, define o descritor de segurança para a pasta.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma pasta de tarefas a fim de permitir ou negar o acesso de determinados usuários e grupos a uma pasta de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





