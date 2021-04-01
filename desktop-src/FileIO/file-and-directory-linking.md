---
description: 'Há dois tipos de links com suporte no sistema de arquivos NTFS: links físicos e junções.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Vinculação de arquivos e diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922633"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="9fbb6-103">Vinculação de arquivos e diretórios</span><span class="sxs-lookup"><span data-stu-id="9fbb6-103">File and Directory Linking</span></span>

<span data-ttu-id="9fbb6-104">O sistema de arquivos NTFS fornece a capacidade de criar uma representação de sistema de um arquivo ou diretório em um local na estrutura de diretório que é diferente do objeto de arquivo ou diretório ao qual está sendo vinculado.</span><span class="sxs-lookup"><span data-stu-id="9fbb6-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="9fbb6-105">Esse processo é chamado de vinculação.</span><span class="sxs-lookup"><span data-stu-id="9fbb6-105">This process is called linking.</span></span> <span data-ttu-id="9fbb6-106">Há dois tipos de links com suporte no sistema de arquivos NTFS: [links físicos e junções](hard-links-and-junctions.md).</span><span class="sxs-lookup"><span data-stu-id="9fbb6-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="9fbb6-107">O sistema de arquivos NTFS também fornece o [serviço Distributed Link Tracking](distributed-link-tracking-and-object-identifiers.md), que rastreia automaticamente os links conforme eles são movidos.</span><span class="sxs-lookup"><span data-stu-id="9fbb6-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fbb6-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9fbb6-108">In this section</span></span>



| <span data-ttu-id="9fbb6-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="9fbb6-109">Topic</span></span>                                                                                                               | <span data-ttu-id="9fbb6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fbb6-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fbb6-111">Links físicos e junções</span><span class="sxs-lookup"><span data-stu-id="9fbb6-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="9fbb6-112">Descreve links e junções difíceis.</span><span class="sxs-lookup"><span data-stu-id="9fbb6-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="9fbb6-113">Rastreamento de link distribuído e identificadores de objeto</span><span class="sxs-lookup"><span data-stu-id="9fbb6-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="9fbb6-114">O **serviço Distributed Link Tracking** permite que os aplicativos cliente acompanhem as fontes de link que foram movidas.</span><span class="sxs-lookup"><span data-stu-id="9fbb6-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




