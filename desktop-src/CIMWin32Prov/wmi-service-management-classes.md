---
description: As classes de gerenciamento de serviço WMI são usadas para gerenciar o próprio serviço WMI e não o sistema de computador ou a rede corporativa. O gerenciamento do WMI abrange tanto a configuração do serviço WMI quanto o gerenciamento de operações do WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classes de gerenciamento de serviço WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088961"
---
# <a name="wmi-service-management-classes"></a>Classes de gerenciamento de serviço WMI

As classes de gerenciamento de serviço WMI são usadas para gerenciar o próprio serviço WMI e não o sistema de computador ou a rede corporativa. O gerenciamento do WMI abrange tanto a configuração do serviço WMI quanto o gerenciamento de operações do WMI.

A categoria gerenciamento de serviços WMI inclui as seguintes subcategorias de classes:

-   [Classes de configuração do WMI](#wmi-configuration-classes)
-   [Classes de gerenciamento do WMI](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a>Classes de configuração do WMI

A classe de configuração do WMI deriva métodos que configuram o serviço WMI.

Veja a seguir uma tabela de classes de configuração do WMI.



| Classe                                                             | Descrição                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_MethodParameterClass Win32**](win32-methodparameterclass.md) | Abstrata, classe base que implementa parâmetros de método derivados desta classe. |



 

## <a name="wmi-management-classes"></a>Classes de gerenciamento do WMI

As classes de gerenciamento do WMI representam parâmetros operacionais para o serviço WMI.

Veja a seguir uma tabela de classes de gerenciamento de WMI.



| Classe                                                       | Descrição                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_WMISetting Win32**](win32-wmisetting.md)               | Contém os parâmetros operacionais para o serviço WMI.                                      |
| [**\_WMIElementSetting Win32**](win32-wmielementsetting.md) | Associação entre um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes Win32](./win32-provider.md)
</dt> </dl>

 

 
