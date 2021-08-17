---
title: Propriedade TaskSettings.NetworkSettings
description: Para scripts, obtém ou define o objeto de configurações de rede que contém um nome e um identificador de perfil de rede.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Propriedade NetworkSettings Agendador de Tarefas
- Propriedade NetworkSettings Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , NetworkSettings
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
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059645"
---
# <a name="tasksettingsnetworksettings-property"></a>Propriedade TaskSettings.NetworkSettings

Para scripts, obtém ou define o objeto de configurações de rede que contém um nome e um identificador de perfil de rede. Se a propriedade [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) for **True** e um propfile de rede for especificado na propriedade **NetworkSettings,** a tarefa será executado somente se o perfil de rede especificado estiver disponível.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto NetworkSettings**](networksettings.md) que contém um nome e um identificador de perfil de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





