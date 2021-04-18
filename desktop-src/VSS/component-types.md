---
description: Os componentes indicam a espécie de dados que eles representam por meio de um tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipos de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781335"
---
# <a name="component-types"></a><span data-ttu-id="93adb-103">Tipos de componentes</span><span class="sxs-lookup"><span data-stu-id="93adb-103">Component Types</span></span>

<span data-ttu-id="93adb-104">Os componentes indicam a espécie de dados que eles representam por meio de um tipo.</span><span class="sxs-lookup"><span data-stu-id="93adb-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="93adb-105">Atualmente, os tipos de componentes (consulte [**\_ \_ tipo de componente do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) são limitados ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="93adb-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="93adb-106">Componentes de banco de dados</span><span class="sxs-lookup"><span data-stu-id="93adb-106">Database components</span></span>
-   <span data-ttu-id="93adb-107">Grupos de arquivos</span><span class="sxs-lookup"><span data-stu-id="93adb-107">File groups</span></span>

<span data-ttu-id="93adb-108">Para obter informações de implementação sobre como definir tipos de componentes, consulte [definição de componentes por gravadores](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="93adb-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="93adb-109">Os gravadores têm uma digitação de dados que indica seu uso (consulte [**\_ \_ tipo de origem VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), que pode ser o seguinte:</span><span class="sxs-lookup"><span data-stu-id="93adb-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="93adb-110">Um banco de dados transacional (como um SQL Server)</span><span class="sxs-lookup"><span data-stu-id="93adb-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="93adb-111">Um banco de dados não transacional (como um cliente de planilha)</span><span class="sxs-lookup"><span data-stu-id="93adb-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="93adb-112">Grupo de arquivos (outro)</span><span class="sxs-lookup"><span data-stu-id="93adb-112">File group (other)</span></span>

<span data-ttu-id="93adb-113">Especificar um tipo de componente como banco de dados permite a identificação mais fácil de seu conteúdo, permite a manipulação separada de arquivos de log e de dados (consulte [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para obter detalhes) e impõe maior rigor na seleção de arquivo, não permitindo a seleção de arquivo recursivo ou o uso de um [*caminho alternativo*](vssgloss-a.md) (consulte [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) e [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span><span class="sxs-lookup"><span data-stu-id="93adb-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="93adb-114">Com um componente de grupo de arquivos, por outro lado, ao preço de não saber quais dados ele contém, você tem maior liberdade sobre como os arquivos são inseridos, pois você pode usar especificação recursiva e caminhos alternativos.</span><span class="sxs-lookup"><span data-stu-id="93adb-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="93adb-115">Tipos de componentes adicionais podem ser adicionados no futuro.</span><span class="sxs-lookup"><span data-stu-id="93adb-115">Additional component types may be added in the future.</span></span>

 

 



