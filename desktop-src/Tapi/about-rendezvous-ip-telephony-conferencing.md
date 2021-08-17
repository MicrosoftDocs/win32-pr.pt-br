---
description: Os controles tapi 3 De reunião fornecem mecanismos para anunciar e descobrir conferências de IP multimídia multipartes. O exemplo a seguir descreve um conjunto de componentes e interfaces Component Object Model (COM) para implementar a conferência.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Sobre a conferência de telefonia IP de reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225f7842e0f7efdb97dcadc3d59adc8fa7e5adf0f73cd824b335500a5aa6c11d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949273"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Sobre a conferência de telefonia IP de reunião

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

Os controles tapi 3 De reunião fornecem mecanismos para anunciar e descobrir conferências de IP multimídia multipartes. O exemplo a seguir descreve um conjunto de componentes e interfaces Component Object Model (COM) para implementar a conferência.

COM é o modelo de codificação básico para TAPI 3 e a familiaridade com ele é assumida neste documento. Para obter informações sobre COM, pesquise o SDK (Kit de Desenvolvimento de Software de Plataforma).

## <a name="features"></a>Recursos

-   Fornece a abstração de um diretório de conferência para manipular anúncios de conferências multimídia
-   Fornece segurança por meio de autenticação, criptografia e uma ACL (camada de controle de acesso) por comunicado
-   Fornece um esquema comum para um comunicado de conferência, permitindo pesquisas por valores de atributo
-   Permite extensões por meio de um atributo mantido pelo provedor (blob de conferência) no esquema
-   Fornece um wrapper COM para a API de alocação de endereço multicast (MADCAP)

## <a name="architecture"></a>Arquitetura

As descrições e o diagrama a seguir ilustram os principais aspectos da arquitetura do sistema.

-   O cliente pode manipular conferências armazenadas em um diretório dinâmico ILS ou servidor NTDS usando controles De reunião. O protocolo LDAP é usado para se comunicar com um servidor ILS.
-   Os controles De reunião fornecem interfaces COM duplas para scripts e programação.
-   Um servidor SAP (Session Announcement Protocol) com acesso direto à Internet escuta anúncios de conferência na Internet e popula servidores dinâmicos ILS com as informações da conferência. Da mesma forma, ele também anuncia as conferências criadas localmente cujo escopo inclui a Internet. (O servidor SAP não está planejado para o Microsoft Windows 2000.)

![arquitetura do sistema de reunião](images/rend1.png)

 

 



