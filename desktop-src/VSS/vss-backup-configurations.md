---
description: Há vários tipos de backup com suporte em Convenção&\# 8212; incremental, diferencial e completa&\# 8212; que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurações de backup do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781078"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="de8b4-103">Configurações de backup do VSS</span><span class="sxs-lookup"><span data-stu-id="de8b4-103">VSS Backup Configurations</span></span>

<span data-ttu-id="de8b4-104">Há vários tipos de backup com suporte de Convenção – incremental, diferencial e completo – que o VSS reconhece, bem como uma configuração de backup peculiar para o VSS.</span><span class="sxs-lookup"><span data-stu-id="de8b4-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="de8b4-105">Ao definir uma configuração de backup, um solicitante e os gravadores em um sistema indicam como os dados serão gravados em um dispositivo de armazenamento, como o mecanismo de cópia de sombra será implantado e quais informações precisam ser salvas.</span><span class="sxs-lookup"><span data-stu-id="de8b4-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="de8b4-106">A interação entre escritores e solicitantes é determinada pelo tipo de backup que um solicitante deseja executar e os tipos (ou esquemas) aos quais cada gravador pode dar suporte:</span><span class="sxs-lookup"><span data-stu-id="de8b4-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="de8b4-107">Estado de backup do VSS</span><span class="sxs-lookup"><span data-stu-id="de8b4-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="de8b4-108">Suporte ao esquema de backup do gravador</span><span class="sxs-lookup"><span data-stu-id="de8b4-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="de8b4-109">Suporte a esquema de nível de arquivo</span><span class="sxs-lookup"><span data-stu-id="de8b4-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



