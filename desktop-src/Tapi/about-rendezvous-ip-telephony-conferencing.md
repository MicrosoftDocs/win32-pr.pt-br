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
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="4b88c-104">Sobre a conferência de telefonia IP da reunião</span><span class="sxs-lookup"><span data-stu-id="4b88c-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="4b88c-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b88c-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b88c-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4b88c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b88c-107">Os controles de reunião TAPI 3 fornecem mecanismos para anunciar e descobrir conferências de IP de multimídia multiparte.</span><span class="sxs-lookup"><span data-stu-id="4b88c-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="4b88c-108">Veja a seguir uma descrição de um conjunto de componentes e interfaces do Component Object Model (COM) para implementar a conferência.</span><span class="sxs-lookup"><span data-stu-id="4b88c-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="4b88c-109">O COM é o modelo de codificação básico para a TAPI 3, e familiaridade com ele é assumida em todo este documento.</span><span class="sxs-lookup"><span data-stu-id="4b88c-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="4b88c-110">Para obter informações sobre COM, pesquise o kit de desenvolvimento de software de plataforma (SDK).</span><span class="sxs-lookup"><span data-stu-id="4b88c-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="4b88c-111">Recursos</span><span class="sxs-lookup"><span data-stu-id="4b88c-111">Features</span></span>

-   <span data-ttu-id="4b88c-112">Fornece a abstração de um diretório de conferência para manipular anúncios de conferências de multimídia</span><span class="sxs-lookup"><span data-stu-id="4b88c-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="4b88c-113">Fornece segurança por meio de autenticação, criptografia e uma camada de controle de acesso por anúncio (ACL)</span><span class="sxs-lookup"><span data-stu-id="4b88c-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="4b88c-114">Fornece um esquema comum para um comunicado de conferência, permitindo pesquisas por valores de atributo</span><span class="sxs-lookup"><span data-stu-id="4b88c-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="4b88c-115">Permite extensões por meio de um atributo mantido pelo provedor (blob de conferência) no esquema</span><span class="sxs-lookup"><span data-stu-id="4b88c-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="4b88c-116">Fornece um wrapper COM para a API de alocação de endereço multicast (MADCAP)</span><span class="sxs-lookup"><span data-stu-id="4b88c-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="4b88c-117">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="4b88c-117">Architecture</span></span>

<span data-ttu-id="4b88c-118">As descrições e o diagrama a seguir ilustram os principais aspectos da arquitetura do sistema.</span><span class="sxs-lookup"><span data-stu-id="4b88c-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="4b88c-119">O cliente pode manipular conferências armazenadas em um diretório do ILS ou no servidor NTDS usando os controles de reunião.</span><span class="sxs-lookup"><span data-stu-id="4b88c-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="4b88c-120">O protocolo LDAP (Lightweight Directory Access Protocol) é usado para se comunicar com um servidor ILS.</span><span class="sxs-lookup"><span data-stu-id="4b88c-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="4b88c-121">Os controles de reunião fornecem interfaces COM duplas para scripts e programação.</span><span class="sxs-lookup"><span data-stu-id="4b88c-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="4b88c-122">Um servidor SAP (Session Announcement Protocol) com acesso direto à Internet escuta anúncios de conferência na Internet e preenche os servidores dinâmicos do ILS com as informações da conferência.</span><span class="sxs-lookup"><span data-stu-id="4b88c-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="4b88c-123">Da mesma forma, ele também anuncia as conferências criadas localmente cujo escopo inclui a Internet.</span><span class="sxs-lookup"><span data-stu-id="4b88c-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="4b88c-124">(O servidor SAP não está planejado para o Microsoft Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="4b88c-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![arquitetura do sistema de reunião](images/rend1.png)

 

 



