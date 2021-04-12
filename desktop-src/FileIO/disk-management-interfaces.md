---
description: Interfaces usadas no gerenciamento de disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gerenciamento de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171144"
---
# <a name="disk-management-interfaces"></a>Interfaces de gerenciamento de disco

As interfaces a seguir são usadas no gerenciamento de disco.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                     | Descrição                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controla os recursos de cota de disco de um único volume do sistema de arquivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Recebe notificações de eventos relacionadas à cota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Representa uma entrada de cota de usuário único no arquivo de informações de cota de volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Adiciona vários objetos de usuário de cota a um contêiner que é enviado para atualização em uma única chamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera as entradas de cota do usuário no volume.<br/>                                                        |



 

 

