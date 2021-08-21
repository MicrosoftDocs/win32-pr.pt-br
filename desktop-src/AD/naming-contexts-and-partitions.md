---
title: Nomeando contextos e partições de diretório
description: Cada controlador de domínio em uma floresta de domínio controlada por Active Directory Domain Services inclui partições de diretório.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Nomeando contextos e aD de partições de diretório
- Contextos de nomentura AD , Sobre
- AD de partições de diretório, Sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309b76b50270f093b3a4930680b343d517976e269e731082696b89bf6a58c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025704"
---
# <a name="naming-contexts-and-directory-partitions"></a>Nomeando contextos e partições de diretório

Cada controlador de domínio em uma floresta de domínio controlada por Active Directory Domain Services inclui [*partições de diretório*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). As partições de diretório também são [*conhecidas como contextos de nomen entre .*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)) Uma partição de diretório é uma parte contígua do diretório geral que tem escopo de replicação independente e dados de agendamento. Por padrão, o serviço Domínio do Active Directory para uma empresa contém as seguintes partições:

-   [*Partição de Esquema:*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85))a partição de esquema contém os objetos **classSchema** e **attributeSchema** que definem os tipos de objetos que podem existir na floresta. Cada controlador de domínio na floresta tem uma réplica da mesma partição de esquema.
-   [*Partição de Configuração:*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85))a partição de configuração contém a topologia de replicação e outros dados de configuração que devem ser replicados em toda a floresta. Cada controlador de domínio na floresta tem uma réplica da mesma partição de configuração.
-   [*Partição de*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))Domínio: a partição de domínio contém os objetos de diretório, como usuários e computadores, associados ao domínio local. Um domínio pode ter vários controladores de domínio e uma floresta pode ter vários domínios. Cada controlador de domínio armazena uma réplica completa da partição de domínio para seu domínio local, mas não armazena réplicas das partições de domínio para outros domínios.

Windows O Server 2003 apresenta a Partição do Diretório do *Aplicativo,* que fornece a capacidade de controlar o escopo da replicação e permitir o posicionamento de réplicas de maneira mais adequada para dados dinâmicos. Para obter mais informações sobre partições de diretório do aplicativo, consulte [About Application Directory Partitions](about-application-directory-partitions.md).

Para obter mais informações sobre como Active Directory Domain Services consistência entre as várias réplicas de uma partição de diretório, consulte [Replication and Data Integrity](replication-and-data-integrity.md).

 

 