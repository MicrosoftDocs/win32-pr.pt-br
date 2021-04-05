---
description: O banco de dados de Windows Installer consiste em muitas tabelas inter-relacionadas que juntos compõem um banco de dados relacional das informações necessárias para instalar um grupo de aplicativos.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Sobre o banco de dados do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828097"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="626e4-103">Sobre o banco de dados do instalador</span><span class="sxs-lookup"><span data-stu-id="626e4-103">About the Installer Database</span></span>

<span data-ttu-id="626e4-104">O banco de dados de Windows Installer consiste em muitas tabelas inter-relacionadas que juntos compõem um banco de dados relacional das informações necessárias para instalar um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="626e4-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="626e4-105">Uma vez que o banco de dados é relacional, as tabelas são vinculadas por meio do dado nos valores de chave primária e estrangeira.</span><span class="sxs-lookup"><span data-stu-id="626e4-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="626e4-106">Isso fornece um método eficiente para alterar o processo de instalação e significa que os usuários podem personalizar mais facilmente um aplicativo ou grupo de aplicativos grande.</span><span class="sxs-lookup"><span data-stu-id="626e4-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="626e4-107">As tabelas de banco de dados refletem o layout geral de todo o grupo de aplicativos, incluindo:</span><span class="sxs-lookup"><span data-stu-id="626e4-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="626e4-108">Recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="626e4-108">Available features</span></span>
-   <span data-ttu-id="626e4-109">Componentes</span><span class="sxs-lookup"><span data-stu-id="626e4-109">Components</span></span>
-   <span data-ttu-id="626e4-110">Relação entre recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="626e4-110">Relationship between features and components</span></span>
-   <span data-ttu-id="626e4-111">Configurações necessárias do registro</span><span class="sxs-lookup"><span data-stu-id="626e4-111">Necessary registry settings</span></span>
-   <span data-ttu-id="626e4-112">Interface do usuário para o aplicativo</span><span class="sxs-lookup"><span data-stu-id="626e4-112">User interface for the application</span></span>

<span data-ttu-id="626e4-113">Para criar um banco de dados de instalação, você deve preencher as tabelas com todas as informações sobre os aplicativos e o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="626e4-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="626e4-114">A criação manual de todas essas tabelas torna-se uma tarefa grande mesmo para uma instalação de tamanho moderado; Portanto, algumas ferramentas de terceiros estão disponíveis para ajudar na criação do banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="626e4-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="626e4-115">As seções a seguir descrevem grupos de tabelas de banco de dados relacionadas.</span><span class="sxs-lookup"><span data-stu-id="626e4-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="626e4-116">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="626e4-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="626e4-117">Grupo de tabelas de arquivos</span><span class="sxs-lookup"><span data-stu-id="626e4-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="626e4-118">Grupo de tabelas do registro</span><span class="sxs-lookup"><span data-stu-id="626e4-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="626e4-119">Grupo de tabelas do sistema</span><span class="sxs-lookup"><span data-stu-id="626e4-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="626e4-120">Grupo de tabelas do localizador</span><span class="sxs-lookup"><span data-stu-id="626e4-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="626e4-121">Grupo de tabelas de informações do programa</span><span class="sxs-lookup"><span data-stu-id="626e4-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="626e4-122">Grupo de tabelas de procedimento de instalação</span><span class="sxs-lookup"><span data-stu-id="626e4-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="626e4-123">Legenda do diagrama de relação de entidade</span><span class="sxs-lookup"><span data-stu-id="626e4-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="626e4-124">Arquivos mortos de texto</span><span class="sxs-lookup"><span data-stu-id="626e4-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="626e4-125">Para obter uma lista completa de todas as tabelas em um banco de dados de instalação, consulte [tabelas de banco de dados](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="626e4-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="626e4-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="626e4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="626e4-127">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="626e4-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



