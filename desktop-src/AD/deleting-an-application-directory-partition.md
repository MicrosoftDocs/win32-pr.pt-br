---
title: Excluindo uma partição de diretório de aplicativo
description: Uma partição de diretório de aplicativo é excluída com a exclusão do objeto crossRef que representa a partição de diretório de aplicativo.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Excluindo um AD de partição de diretório de aplicativo
- AD de partições de diretório de aplicativo, excluindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640418"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="89fa9-105">Excluindo uma partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="89fa9-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="89fa9-106">Uma partição de diretório de aplicativo é excluída com a exclusão do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89fa9-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="89fa9-107">Quando a exclusão do objeto **crossRef** é replicada para um controlador de domínio que tem uma réplica da partição de diretório do aplicativo, o KCC excluirá a réplica local da partição de diretório do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89fa9-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="89fa9-108">Isso eventualmente faz com que todas as réplicas da partição de diretório do aplicativo sejam excluídas.</span><span class="sxs-lookup"><span data-stu-id="89fa9-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="89fa9-109">Quando o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) for excluído, o servidor de Active Directory excluirá o objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) que foi criado quando a partição de diretório de aplicativo foi criada, bem como excluirá todos os objetos na partição de diretório de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89fa9-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="89fa9-110">Nenhum dos objetos na partição de diretório de aplicativo é marcado para exclusão quando eles foram excluídos.</span><span class="sxs-lookup"><span data-stu-id="89fa9-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="89fa9-111">Quando uma partição de diretório de aplicativo é excluída, é muito difícil restaurá-la.</span><span class="sxs-lookup"><span data-stu-id="89fa9-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="89fa9-112">Para restaurar uma partição de diretório de aplicativo, é necessário restaurar um backup que tenha uma réplica da partição de diretório de aplicativo, localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo e restaurar o objeto **crossRef** com autoridade.</span><span class="sxs-lookup"><span data-stu-id="89fa9-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="89fa9-113">**Para excluir uma partição de diretório de aplicativos e suas réplicas, execute as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="89fa9-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="89fa9-114">Pesquise o contêiner partições para obter um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome distinto da partição de diretório do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89fa9-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="89fa9-115">Exclua o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .</span><span class="sxs-lookup"><span data-stu-id="89fa9-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="89fa9-116">Para obter mais informações, consulte [código de exemplo para excluir uma partição de diretório de aplicativo](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="89fa9-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 