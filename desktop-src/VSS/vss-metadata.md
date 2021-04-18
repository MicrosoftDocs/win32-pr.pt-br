---
description: Os gravadores e os solicitantes mantêm as informações necessárias para uma operação de backup ou restauração em seus próprios documentos de metadados.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadados do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763410"
---
# <a name="vss-metadata"></a><span data-ttu-id="cd535-103">Metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="cd535-103">VSS Metadata</span></span>

<span data-ttu-id="cd535-104">Os gravadores e os solicitantes mantêm as informações necessárias para uma operação de backup ou restauração em seus próprios documentos de metadados.</span><span class="sxs-lookup"><span data-stu-id="cd535-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="cd535-105">Esses documentos, o [*documento de metadados do gravador*](vssgloss-w.md) e o [*documento de componentes de backup*](vssgloss-b.md), respectivamente, são usados como base para comunicação e coordenação do gravador e do solicitante durante as atividades de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="cd535-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="cd535-106">Os metadados são representados em formato XML usando um esquema proprietário.</span><span class="sxs-lookup"><span data-stu-id="cd535-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="cd535-107">Os metadados podem ser copiados em disco, fita ou em qualquer outro dispositivo de armazenamento em massa.</span><span class="sxs-lookup"><span data-stu-id="cd535-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="cd535-108">Ele sempre deve ser salvo na mídia de backup durante uma operação de backup e precisará ser recuperado dessa mídia no decorrer de uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="cd535-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="cd535-109">**Cuidado:** Os detalhes específicos do formato e do esquema são apenas para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="cd535-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="cd535-110">Os desenvolvedores não devem tentar modificar ou usar diretamente a representação XML dos metadados.</span><span class="sxs-lookup"><span data-stu-id="cd535-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="cd535-111">Gravadores e solicitantes são fornecidos com uma variedade de métodos de consulta e definição para acessar e modificar os componentes de backup e os documentos de metadados do gravador:</span><span class="sxs-lookup"><span data-stu-id="cd535-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="cd535-112">Trabalhando com o documento de metadados do gravador</span><span class="sxs-lookup"><span data-stu-id="cd535-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="cd535-113">Trabalhando com o documento de componentes de backup</span><span class="sxs-lookup"><span data-stu-id="cd535-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="cd535-114">Componentes de metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="cd535-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



