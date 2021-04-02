---
title: Propriedade TaskSettings. NetworkSettings
description: Para scripts, Obtém ou define o objeto de configurações de rede que contém um nome e identificador de perfil de rede.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Agendador de Tarefas da propriedade NetworkSettings
- Propriedade NetworkSettings Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644381"
---
# <a name="tasksettingsnetworksettings-property"></a>Propriedade TaskSettings. NetworkSettings

Para scripts, Obtém ou define o objeto de configurações de rede que contém um nome e identificador de perfil de rede. Se a propriedade [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) for **true** e um propfile de rede for especificado na propriedade **NetworkSettings** , a tarefa será executada somente se o perfil de rede especificado estiver disponível.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**NetworkSettings**](networksettings.md) que contém um identificador e nome de perfil de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





