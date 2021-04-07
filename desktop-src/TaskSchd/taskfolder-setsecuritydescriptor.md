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
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918216"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





