---
title: Contextos de nomenclatura e partições de diretório
description: Cada controlador de domínio em uma floresta de domínio controlada pelo Active Directory Domain Services inclui partições de diretório.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Contextos de nomenclatura e partições de diretório AD
- Nomeando o anúncio de contextos, sobre
- Partições de diretório AD, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39934f0236e927bff281230c41a303f5e6d2bb0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917114"
---
# <a name="naming-contexts-and-directory-partitions"></a>Contextos de nomenclatura e partições de diretório

Cada controlador de domínio em uma floresta de domínio controlada pelo Active Directory Domain Services inclui [*partições de diretório*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). As partições de diretório também são conhecidas como [*contextos de nomenclatura*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)). Uma partição de diretório é uma parte contígua do diretório geral que tem um escopo de replicação independente e dados de agendamento. Por padrão, o serviço de Domínio do Active Directory para uma empresa contém as seguintes partições:

-   [*Partição de esquema*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85)): a partição de esquema contém os objetos **classSchema** e **attributeSchema** que definem os tipos de objetos que podem existir na floresta. Cada controlador de domínio na floresta tem uma réplica da mesma partição de esquema.
-   [*Partição de configuração*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85)): a partição de configuração contém a topologia de replicação e outros dados de configuração que devem ser replicados em toda a floresta. Cada controlador de domínio na floresta tem uma réplica da mesma partição de configuração.
-   [*Partição de domínio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)): a partição de domínio contém os objetos de diretório, como usuários e computadores, associados ao domínio local. Um domínio pode ter vários controladores de domínio e uma floresta pode ter vários domínios. Cada controlador de domínio armazena uma réplica completa da partição de domínio para seu domínio local, mas não armazena réplicas das partições de domínio para outros domínios.

O Windows Server 2003 apresenta a *partição de diretório de aplicativos*, que fornece a capacidade de controlar o escopo da replicação e permitir o posicionamento de réplicas de uma maneira mais adequada para dados dinâmicos. Para obter mais informações sobre partições de diretório de aplicativos, consulte [sobre partições de diretório de aplicativo](about-application-directory-partitions.md).

Para obter mais informações sobre como Active Directory Domain Services manter a consistência entre as várias réplicas de uma partição de diretório, consulte [replicação e integridade de dados](replication-and-data-integrity.md).

 

 