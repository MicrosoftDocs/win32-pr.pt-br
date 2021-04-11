---
title: Acessando Active Directory usando Visual Basic
description: Um dos recursos mais poderosos que se tornaram disponíveis com o sistema operacional Microsoft Windows 2000 é o serviço de diretório do Microsoft Active Directory.
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- Acessando Active Directory usando Visual Basic ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004887"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="24082-104">Acessando Active Directory usando Visual Basic</span><span class="sxs-lookup"><span data-stu-id="24082-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="24082-105">Um dos recursos mais poderosos que se tornaram disponíveis com o sistema operacional Microsoft Windows 2000 é o serviço de diretório do Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24082-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="24082-106">Quando você faz logon em um domínio do Windows 2000, o Active Directory é colocado em ação; para pesquisar a impressora de cores mais próxima em seu edifício, você pode usar Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24082-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="24082-107">Ele pode ser usado para uma pesquisa de catálogo de endereços ou uma pesquisa de usuários que trabalham na compilação de 40.</span><span class="sxs-lookup"><span data-stu-id="24082-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="24082-108">Com Active Directory, você pode usar um cartão inteligente para fazer logon em um domínio do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="24082-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="24082-109">Você pode até mesmo unir dados de Microsoft SQL Server software de banco de dado e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24082-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="24082-110">Muitas outras tecnologias da Microsoft, como o servidor de fila de mensagens da Microsoft (MSMQ), COM (armazenamento de classe), IPsec (Internet Protocol Security), GPOs (Política de Grupo Objects) e Exchange, são integradas ao Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24082-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="24082-111">Esta seção discute como usar o ADSI (Active Directory Service Interfaces) para acessar Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24082-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="24082-112">Usando um cenário para uma empresa fictícia – a Fabrikam Corporation — você aprenderá a executar algumas tarefas administrativas básicas.</span><span class="sxs-lookup"><span data-stu-id="24082-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="24082-113">À medida que você progride nesse cenário, os exemplos de código em cada seção se baseiam.</span><span class="sxs-lookup"><span data-stu-id="24082-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="24082-114">Para resumir, todos os exemplos de código são escritos com o sistema de desenvolvimento Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="24082-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="24082-115">Para obter mais informações sobre conversão de C++, consulte [mapeando código ADSI Visual Basic para código C++](mapping-adsi-visual-basic-code-to-c-code.md).</span><span class="sxs-lookup"><span data-stu-id="24082-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




