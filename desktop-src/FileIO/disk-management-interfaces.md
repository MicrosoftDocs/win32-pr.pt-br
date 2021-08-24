---
description: Interfaces usadas no gerenciamento de disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gerenciamento de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823206"
---
# <a name="disk-management-interfaces"></a>Interfaces de gerenciamento de disco

As interfaces a seguir são usadas no gerenciamento de disco.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                     | Descrição                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controla os recursos de cota de disco de um único volume do sistema de arquivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Recebe notificações de eventos relacionadas à cota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Representa uma única entrada de cota de usuário no arquivo de informações de cota de volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Adiciona vários objetos de usuário de cota a um contêiner que é enviado para atualização em uma única chamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera entradas de cota de usuário no volume.<br/>                                                        |



 

 

