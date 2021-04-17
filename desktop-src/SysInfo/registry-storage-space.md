---
description: Embora haja poucos limites técnicos para o tipo e o tamanho dos dados que um aplicativo pode armazenar no registro, algumas diretrizes práticas existem para promover a eficiência do sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Espaço de armazenamento do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748372"
---
# <a name="registry-storage-space"></a><span data-ttu-id="7b4c5-103">Espaço de armazenamento do registro</span><span class="sxs-lookup"><span data-stu-id="7b4c5-103">Registry Storage Space</span></span>

<span data-ttu-id="7b4c5-104">Embora haja poucos limites técnicos para o tipo e o tamanho dos dados que um aplicativo pode armazenar no registro, algumas diretrizes práticas existem para promover a eficiência do sistema.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="7b4c5-105">Um aplicativo deve armazenar dados de configuração e inicialização no registro e armazenar outros tipos de dados em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="7b4c5-106">Em geral, os dados que consistem em mais de um ou dois kilobytes (K) devem ser armazenados como um arquivo e referenciados usando uma chave no registro em vez de serem armazenados como um valor.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="7b4c5-107">Em vez de duplicar grandes partes de dados no registro, um aplicativo deve salvar os dados como um arquivo e fazer referência ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="7b4c5-108">O código binário executável nunca deve ser armazenado no registro.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="7b4c5-109">Uma entrada de valor usa muito menos espaço do registro do que uma chave.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="7b4c5-110">Para economizar espaço, um aplicativo deve agrupar dados semelhantes como uma estrutura e armazenar a estrutura como um valor, em vez de armazenar cada um dos membros da estrutura como uma chave separada.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="7b4c5-111">(Armazenar os dados em formato binário permite que um aplicativo armazene dados em um valor que, de outra forma, seria composto de vários tipos incompatíveis.)</span><span class="sxs-lookup"><span data-stu-id="7b4c5-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="7b4c5-112">As exibições dos arquivos do registro são mapeadas na memória do pool paginável.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="7b4c5-113">**Windows server 2008 para 32 bits, Windows Vista com SP1 para 32-bit, Windows Vista, Windows Server 2003, Windows XP:** As exibições dos arquivos de registro são mapeadas no espaço de endereço de cache do computador.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="7b4c5-114">Portanto, independentemente do tamanho dos dados do registro, não é cobrado mais de 4 megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="7b4c5-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="7b4c5-115">O tamanho máximo de um hive de registro é 2 GB, exceto o hive do sistema.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="7b4c5-116">**Windows server 2003 com SP1, Windows server 2003 e Windows XP:** Não há limites explícitos na quantidade total de espaço que pode ser consumida por Hives na memória do pool paginável e no espaço em disco, embora as cotas do sistema possam afetar o tamanho máximo real.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="7b4c5-117">O tamanho máximo de um hive do registro foi limitado a 2 GB a partir do Windows Server 2003 com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7b4c5-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="7b4c5-118">O tamanho máximo do hive do sistema é limitado pela memória física, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="7b4c5-119">Sistema</span><span class="sxs-lookup"><span data-stu-id="7b4c5-119">System</span></span>                      | <span data-ttu-id="7b4c5-120">Tamanho máximo do hive do sistema</span><span class="sxs-lookup"><span data-stu-id="7b4c5-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4c5-121">sistemas baseados em x86</span><span class="sxs-lookup"><span data-stu-id="7b4c5-121">x86-based systems</span></span>           | <span data-ttu-id="7b4c5-122">50 por cento da memória física, até 400 MB. **Windows server 2003 com SP2, Windows server 2003 com SP1, Windows server 2003 e Windows XP:** 25% da memória física, até 200 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="7b4c5-123">sistemas baseados em x64</span><span class="sxs-lookup"><span data-stu-id="7b4c5-123">x64-based systems</span></span>           | <span data-ttu-id="7b4c5-124">50 por cento da memória física, até 1,5 GB. **Windows Server 2003 com SP2:** 25% da memória do sistema, até 200 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="7b4c5-125">**Windows server 2003 com SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="7b4c5-126">Sistemas Intel baseados em Itanium</span><span class="sxs-lookup"><span data-stu-id="7b4c5-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="7b4c5-127">50 por cento da memória física, até 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 com SP2, Windows Server 2003 com SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="7b4c5-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7b4c5-128">Windows 2000</span></span>

<span data-ttu-id="7b4c5-129">Os dados do registro são armazenados no pool paginável, uma área de memória física usada para dados do sistema que podem ser gravados no disco quando não estão em uso.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="7b4c5-130">O valor **RegistrySizeLimit** estabelece a quantidade máxima de pool paginável que pode ser consumida por dados de registro de todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="7b4c5-131">Esse valor está localizado na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="7b4c5-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="7b4c5-132">Por padrão, o limite de tamanho do registro é 25 por cento do pool paginado.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="7b4c5-133">(O tamanho padrão do pool paginado é de 32 MB, portanto, é 8 MB.) O sistema garante que o valor mínimo de **RegistrySizeLimit** seja 4 MB e o máximo seja aproximadamente 80% do valor de **PagedPoolSize** .</span><span class="sxs-lookup"><span data-stu-id="7b4c5-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="7b4c5-134">Se o valor dessa entrada for maior que 80% do tamanho do pool paginado, o sistema definirá o tamanho máximo do registro como 80% do tamanho do pool paginado.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="7b4c5-135">Isso impede que o registro consuma espaço necessário pelos processos.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="7b4c5-136">Observe que a definição desse valor não aloca espaço no pool paginável, nem garante que o espaço estará disponível, se necessário.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="7b4c5-137">O tamanho do pool paginado é determinado pelo valor de **PagedPoolSize** na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="7b4c5-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="7b4c5-138">Para obter um exemplo de como determinar os tamanhos atuais e máximos do registro, consulte [determinando o tamanho do registro](determining-the-registry-size.md).</span><span class="sxs-lookup"><span data-stu-id="7b4c5-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="7b4c5-139">O pool de páginas máximos é de aproximadamente 300.470 MB, portanto, o limite de tamanho do registro é de 240-376 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="7b4c5-140">No entanto, se a opção/3GB for usada, o tamanho máximo de pool paginado será de 192 MB, de modo que o registro pode ter um máximo de 153,6 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4c5-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 




