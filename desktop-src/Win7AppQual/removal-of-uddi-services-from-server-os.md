---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Remoção dos serviços UDDI do sistema operacional do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751386"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="19dcc-103">Remoção dos serviços UDDI do sistema operacional do servidor</span><span class="sxs-lookup"><span data-stu-id="19dcc-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="19dcc-104">Plataforma afetada</span><span class="sxs-lookup"><span data-stu-id="19dcc-104">Affected Platform</span></span>

<span data-ttu-id="19dcc-105">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19dcc-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="19dcc-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="19dcc-106">Feature Impact</span></span>

<span data-ttu-id="19dcc-107">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="19dcc-107">**Severity** - Medium</span></span>  
<span data-ttu-id="19dcc-108">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="19dcc-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="19dcc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="19dcc-109">Description</span></span>

<span data-ttu-id="19dcc-110">A Microsoft removeu a função de servidor de serviços UDDI (descrição universal, descoberta e integração) do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="19dcc-111">Versões futuras dos serviços UDDI serão parte do produto Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="19dcc-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="19dcc-112">Esta realinhamento e consolidação do produto posiciona a Microsoft para melhor atender ao mercado SOA (arquitetura orientada a serviços).</span><span class="sxs-lookup"><span data-stu-id="19dcc-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="19dcc-113">A primeira versão posterior ao Windows Server 2008 dos serviços UDDI será compatível com os padrões UDDI v 3.0.</span><span class="sxs-lookup"><span data-stu-id="19dcc-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="19dcc-114">Ele será enviado como parte da versão BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="19dcc-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="19dcc-115">Para atender ao nosso compromisso de fornecer uma experiência de usuário satisfatória, oferecemos um pacote de instalação dos serviços UDDI V3 para o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="19dcc-116">Manifestação</span><span class="sxs-lookup"><span data-stu-id="19dcc-116">Manifestation</span></span>

<span data-ttu-id="19dcc-117">A presença de versões anteriores dos componentes dos serviços UDDI no sistema bloqueia uma atualização para o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="19dcc-118">Mitigação do impacto</span><span class="sxs-lookup"><span data-stu-id="19dcc-118">Mitigation of Impact</span></span>

<span data-ttu-id="19dcc-119">Os usuários que implantaram um site dos serviços UDDI do Windows Server 2003 ou do Windows Server 2008 podem optar por não atualizar os servidores que executam os serviços UDDI para o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="19dcc-120">Eles também podem mover os serviços UDDI para as caixas do Windows Server 2003 ou do Windows Server 2008 dedicadas se precisarem atualizar as caixas de serviços UDDI atuais.</span><span class="sxs-lookup"><span data-stu-id="19dcc-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="19dcc-121">Solução</span><span class="sxs-lookup"><span data-stu-id="19dcc-121">Solution</span></span>

<span data-ttu-id="19dcc-122">A solução recomendada é implantar os serviços UDDI v 3.0 do BizTalk Server 2009 em um computador com Windows Server 2008 R2 e, em seguida, migrar o site antigo para o novo site.</span><span class="sxs-lookup"><span data-stu-id="19dcc-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="19dcc-123">Os serviços UDDI v 3.0 fornecem compatibilidade com versões anteriores com os serviços UDDI 2,0, de modo que qualquer aplicativo que esteja usando os serviços UDDI não será afetado.</span><span class="sxs-lookup"><span data-stu-id="19dcc-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="19dcc-124">Para fazer isso, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="19dcc-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="19dcc-125">Configure um novo site dos serviços UDDI v 3.0 em um computador já carregado com o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="19dcc-126">(Observação: em uma configuração distribuída, um site do UDDI v 3.0 pode consistir em mais de um computador com Windows Server 2008 R2.)</span><span class="sxs-lookup"><span data-stu-id="19dcc-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="19dcc-127">Use a ferramenta de migração de dados UDDI para migrar os dados do banco de dados dos serviços UDDI antigos para o novo banco de dado.</span><span class="sxs-lookup"><span data-stu-id="19dcc-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="19dcc-128">Faça backup do banco de dados dos serviços UDDI antigos para garantir a funcionalidade de reversão.</span><span class="sxs-lookup"><span data-stu-id="19dcc-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="19dcc-129">Desinstale o antigo software de serviços UDDI e, em seguida, atualize essas caixas para o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="19dcc-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="19dcc-130">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="19dcc-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="19dcc-131">Site dos serviços UDDI da Microsoft</span><span class="sxs-lookup"><span data-stu-id="19dcc-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="19dcc-132">Especificações de UDDI</span><span class="sxs-lookup"><span data-stu-id="19dcc-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="19dcc-133">Download dos serviços UDDI v 3.0 para Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19dcc-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



