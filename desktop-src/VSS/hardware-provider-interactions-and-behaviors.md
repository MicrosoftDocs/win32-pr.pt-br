---
description: Interações e comportamentos do provedor de hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interações e comportamentos do provedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c8029b32ee3387b86519da8630d995820bf3dab5da79769ca26f618ef32660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122055"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interações e comportamentos do provedor de hardware

Os provedores de hardware podem dar suporte a cópias de sombra de espelho de cópia completa e/ou de espelhamento completo (diferencial e/ou Plex). A alocação de recursos para cópias de sombra deve seguir o contexto especificado pelo solicitante em [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerado pelo [**\_ \_ \_ contexto de instantâneo VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)para o conjunto de cópias de sombra.

-   Se o solicitante especificar um contexto de cópia de sombra com suporte do provedor, o provedor deverá criar uma cópia de sombra usando esse método.
-   Se o solicitante especificar um contexto de cópia de sombra que não tenha suporte do provedor, o provedor não deverá tentar criar a cópia de sombra e retornar **false** por meio do parâmetro *pbIsSupported* em [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Se o solicitante não especificar explicitamente um contexto de cópia de sombra, o provedor deverá usar um comportamento padrão razoável para a criação da cópia de sombra.

Os provedores de hardware associados aos subsistemas de RAID SAN devem dar suporte a cópias de sombra transportáveis para permitir a movimentação entre hosts em uma SAN.

Os provedores de hardware em execução em vários computadores em uma SAN que ainda gerenciam o mesmo subsistema RAID não precisam coordenar entre os provedores em uma SAN. O coordenador mantém qualquer Estado necessário. Dois tipos de estado são reconhecidos:

-   Estado necessário para dar suporte ao acesso a dados para os volumes contidos em uma cópia de sombra de hardware. Isso inclui qualquer marcação de um volume como somente leitura ou oculto. Esse Estado deve estar no LUN de hardware e viajar com o LUN. Esse estado é preservado entre as épocas de inicialização e/ou a descoberta do dispositivo. O VSS gerencia esse estado durante o tempo de vida da cópia de sombra.
-   Estado necessário para reconhecer um volume específico como parte de um conjunto de cópias de sombra. Esse estado é persistido pelo VSS em conjunto com o solicitante que criou originalmente o conjunto de cópias de sombra.

Para obter mais informações, consulte estes tópicos:

-   [O processo de criação de cópia de sombra](the-shadow-copy-creation-process.md)
-   [Comportamentos necessários para provedores de cópia de sombra](required-behaviors-for-shadow-copy-providers.md)
-   [Transições de estado em provedores de cópia de sombra](state-transitions-in-shadow-copy-providers.md)
-   [Tratamento de erro em provedores de cópia de sombra](error-handling-in-shadow-copy-providers.md)

 

 



