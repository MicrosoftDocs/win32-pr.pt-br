---
description: O grupo de arquivos de tabelas contém todas as tabelas de Windows Installer relacionadas aos arquivos.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Grupo de tabelas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754357"
---
# <a name="file-tables-group"></a><span data-ttu-id="b9600-103">Grupo de tabelas de arquivos</span><span class="sxs-lookup"><span data-stu-id="b9600-103">File Tables Group</span></span>

![grupo de tabelas de arquivos](images/filegrp.png)

<span data-ttu-id="b9600-105">Para obter mais informações sobre este diagrama, consulte a [legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="b9600-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="b9600-106">Um desenvolvedor de pacote do instalador deve considerar popular o grupo de tabelas de arquivos depois de dividir o aplicativo em [componentes e recursos](components-and-features.md) e depois de preencher o [grupo de tabelas principais](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="b9600-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="b9600-107">O grupo de tabelas de arquivos contém todos os arquivos que pertencem à instalação e a maioria desses arquivos é listada na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9600-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="b9600-108">A [tabela de diretórios](directory-table.md) não é mostrada na figura, mas está fortemente relacionada ao grupo de tabelas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b9600-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="b9600-109">A tabela de diretórios fornece a estrutura de diretório da instalação do.</span><span class="sxs-lookup"><span data-stu-id="b9600-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="b9600-110">O grupo de arquivos de tabelas contém todas as tabelas relacionadas aos arquivos.</span><span class="sxs-lookup"><span data-stu-id="b9600-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="b9600-111">A [tabela de arquivos](file-table.md) lista os arquivos que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="b9600-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="b9600-112">Os arquivos que não estão listados na tabela de arquivos incluem arquivos de disco, que são listados na tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9600-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="b9600-113">Como cada arquivo pertence a um componente, a tabela de arquivos tem uma chave externa na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="b9600-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="b9600-114">A [tabela RemoveFile](removefile-table.md) contém uma lista de arquivos a serem removidos pela [ação](removefiles-action.md)removidas.</span><span class="sxs-lookup"><span data-stu-id="b9600-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="b9600-115">A [tabela de fontes](font-table.md) lista os arquivos de fonte a serem registrados com o sistema.</span><span class="sxs-lookup"><span data-stu-id="b9600-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="b9600-116">A [tabela selfreg](selfreg-table.md) lista os arquivos de módulo da instalação autoregistrada.</span><span class="sxs-lookup"><span data-stu-id="b9600-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="b9600-117">A [tabela de mídia](media-table.md) lista a mídia de origem e os discos que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="b9600-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="b9600-118">A [tabela BindImage](bindimage-table.md) lista os arquivos que estão associados a DLLs importadas por executáveis.</span><span class="sxs-lookup"><span data-stu-id="b9600-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="b9600-119">A [tabela MoveFile](movefile-table.md) especifica quais arquivos são movidos durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="b9600-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="b9600-120">A [tabela replicafile](duplicatefile-table.md) especifica quais arquivos são duplicados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="b9600-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="b9600-121">A [tabela inifile](inifile-table.md) lista os arquivos. ini e as informações que o aplicativo precisa definir no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b9600-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="b9600-122">A [tabela RemoveIniFile](removeinifile-table.md) contém as informações que um aplicativo precisa excluir de um arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="b9600-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="b9600-123">A [tabela de ambiente](environment-table.md) é usada para definir os valores de variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9600-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="b9600-124">A [tabela de ícones](icon-table.md) fornece informações de ícone que são copiadas para um arquivo como parte do anúncio do produto.</span><span class="sxs-lookup"><span data-stu-id="b9600-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="b9600-125">A [tabela FileSFPCatalog](filesfpcatalog-table.md) associa arquivos especificados a arquivos de catálogo de proteção de arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="b9600-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="b9600-126">**Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="b9600-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="b9600-127">A [tabela SFPCatalog](sfpcatalog-table.md) contém catálogos de proteção de arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="b9600-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="b9600-128">**Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="b9600-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="b9600-129">A [tabela MsiFileHash](msifilehash-table.md) é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b9600-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



