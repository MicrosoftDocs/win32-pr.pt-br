---
description: Como uma alternativa para criar e configurar partições locais por meio da ferramenta administrativa serviços de componentes, você pode gerenciar partições programaticamente usando coleções e propriedades de administração COM+ específicas de partição.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Gerenciando partições locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920548"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="6db42-103">Gerenciando partições locais</span><span class="sxs-lookup"><span data-stu-id="6db42-103">Managing Local Partitions</span></span>

<span data-ttu-id="6db42-104">Como uma alternativa para criar e configurar partições locais por meio da ferramenta administrativa serviços de componentes, você pode gerenciar partições programaticamente usando coleções e propriedades de administração COM+ específicas de partição.</span><span class="sxs-lookup"><span data-stu-id="6db42-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="6db42-105">O serviço de partições COM+ não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="6db42-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="6db42-106">Para usar o serviço de partições COM+, você deve habilitá-lo por meio da ferramenta de administração de serviços de componentes ou alterando a propriedade PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) para true.</span><span class="sxs-lookup"><span data-stu-id="6db42-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="6db42-107">A seguinte sub-rotina gravada em Visual Basic script demonstra como criar uma partição no computador local:</span><span class="sxs-lookup"><span data-stu-id="6db42-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



<span data-ttu-id="6db42-108">A seguinte sub-rotina gravada em Visual Basic script demonstra como excluir uma partição do computador local:</span><span class="sxs-lookup"><span data-stu-id="6db42-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="6db42-109">A seguinte sub-rotina gravada em Visual Basic script demonstra como definir a partição padrão para um usuário:</span><span class="sxs-lookup"><span data-stu-id="6db42-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="6db42-110">A seguinte sub-rotina gravada em Visual Basic script demonstra como remover a partição padrão de um usuário:</span><span class="sxs-lookup"><span data-stu-id="6db42-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="6db42-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6db42-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db42-112">Coletando métricas de partição</span><span class="sxs-lookup"><span data-stu-id="6db42-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="6db42-113">Configurando o cache de partição</span><span class="sxs-lookup"><span data-stu-id="6db42-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="6db42-114">Agrupando aplicativos em partições</span><span class="sxs-lookup"><span data-stu-id="6db42-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="6db42-115">Gerenciando partições no Active Directory</span><span class="sxs-lookup"><span data-stu-id="6db42-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="6db42-116">Configurando direitos administrativos para uma partição</span><span class="sxs-lookup"><span data-stu-id="6db42-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



