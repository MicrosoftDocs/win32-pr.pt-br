---
description: Um solicitante deve selecionar um provedor específico somente se ele tiver algumas informações sobre os provedores disponíveis.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selecionando provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091424"
---
# <a name="selecting-providers"></a><span data-ttu-id="5d9c5-103">Selecionando provedores</span><span class="sxs-lookup"><span data-stu-id="5d9c5-103">Selecting Providers</span></span>

<span data-ttu-id="5d9c5-104">Um solicitante deve selecionar um provedor específico somente se ele tiver algumas informações sobre os provedores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5d9c5-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="5d9c5-105">Como isso geralmente não será o caso, é recomendável que um solicitante forneça o GUID \_ NULL como uma ID de provedor para [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), que permite ao sistema escolher um provedor de acordo com o seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="5d9c5-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="5d9c5-106">Se um provedor de hardware que dá suporte ao volume especificado estiver disponível, ele será selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d9c5-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="5d9c5-107">Se nenhum provedor de hardware estiver disponível, se qualquer provedor de software específico para o volume especificado estiver disponível, ele será selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d9c5-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="5d9c5-108">Se nenhum provedor de hardware e nenhum provedor de software específico para os volumes estiver disponível, o provedor do sistema será selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d9c5-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="5d9c5-109">No entanto, um solicitante pode obter informações sobre provedores disponíveis usando [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="5d9c5-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="5d9c5-110">Com essas informações, e somente se o aplicativo de backup tiver uma boa compreensão dos vários provedores, um solicitante poderá fornecer uma ID de provedor válida para [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span><span class="sxs-lookup"><span data-stu-id="5d9c5-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="5d9c5-111">Observe que todos os volumes não precisam ter o mesmo provedor.</span><span class="sxs-lookup"><span data-stu-id="5d9c5-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



