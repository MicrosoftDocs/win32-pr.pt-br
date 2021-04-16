---
description: Os controles de reunião TAPI 3 fornecem mecanismos para anunciar e descobrir conferências de IP de multimídia multiparte. Veja a seguir uma descrição de um conjunto de componentes e interfaces do Component Object Model (COM) para implementar a conferência.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Sobre a conferência de telefonia IP da reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550243"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Sobre a conferência de telefonia IP da reunião

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

Os controles de reunião TAPI 3 fornecem mecanismos para anunciar e descobrir conferências de IP de multimídia multiparte. Veja a seguir uma descrição de um conjunto de componentes e interfaces do Component Object Model (COM) para implementar a conferência.

O COM é o modelo de codificação básico para a TAPI 3, e familiaridade com ele é assumida em todo este documento. Para obter informações sobre COM, pesquise o kit de desenvolvimento de software de plataforma (SDK).

## <a name="features"></a>Recursos

-   Fornece a abstração de um diretório de conferência para manipular anúncios de conferências de multimídia
-   Fornece segurança por meio de autenticação, criptografia e uma camada de controle de acesso por anúncio (ACL)
-   Fornece um esquema comum para um comunicado de conferência, permitindo pesquisas por valores de atributo
-   Permite extensões por meio de um atributo mantido pelo provedor (blob de conferência) no esquema
-   Fornece um wrapper COM para a API de alocação de endereço multicast (MADCAP)

## <a name="architecture"></a>Arquitetura

As descrições e o diagrama a seguir ilustram os principais aspectos da arquitetura do sistema.

-   O cliente pode manipular conferências armazenadas em um diretório do ILS ou no servidor NTDS usando os controles de reunião. O protocolo LDAP (Lightweight Directory Access Protocol) é usado para se comunicar com um servidor ILS.
-   Os controles de reunião fornecem interfaces COM duplas para scripts e programação.
-   Um servidor SAP (Session Announcement Protocol) com acesso direto à Internet escuta anúncios de conferência na Internet e preenche os servidores dinâmicos do ILS com as informações da conferência. Da mesma forma, ele também anuncia as conferências criadas localmente cujo escopo inclui a Internet. (O servidor SAP não está planejado para o Microsoft Windows 2000.)

![arquitetura do sistema de reunião](images/rend1.png)

 

 



