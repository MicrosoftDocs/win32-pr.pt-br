---
description: 'Determinadas funcionalidades planejadas para a versão 2003 do Windows Server do VSS não são totalmente suportadas:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restrições no Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198e4ce79da4665bf712a64a466691041d452d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781304"
---
# <a name="restrictions-in-windows-server-2003"></a>Restrições no Windows Server 2003

Determinadas funcionalidades planejadas para a versão 2003 do Windows Server do VSS não são totalmente suportadas:

-   Durante as operações de backup, várias instâncias de uma determinada classe de gravador são permitidas somente se apenas uma dessas instâncias tiver um estado de restauração do gravador (consulte [**VSS \_ WRITERRESTORE \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) diferente do VSS \_ WRE \_ Never. Se essa condição for atendida, todas as instâncias do gravador participarão totalmente durante o backup, gerando documentos de metadados do gravador e participando da manipulação de eventos.
-   Durante as operações de restauração, somente um gravador receberá eventos de restauração gerados pelo solicitante. Se mais de uma instância de uma classe de gravador tiver um estado de restauração do gravador definido como algo diferente do VSS \_ WRE \_ Never, somente uma instância receberá eventos de restauração. Qual instância irá recebê-los é indeterminado.

 

 



