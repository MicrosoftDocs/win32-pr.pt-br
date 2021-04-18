---
description: O registro do sistema contém dados relacionados a recursos.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descrevendo um recurso para o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771571"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="fcd93-103">Descrevendo um recurso para o registro</span><span class="sxs-lookup"><span data-stu-id="fcd93-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="fcd93-104">O registro do sistema contém dados relacionados a recursos.</span><span class="sxs-lookup"><span data-stu-id="fcd93-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="fcd93-105">Esses dados estão localizados na seguinte chave do registro e são mantidos em um tipo de dados de registro especial chamado **reg \_ Resource \_ list**.</span><span class="sxs-lookup"><span data-stu-id="fcd93-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="fcd93-106">Os aplicativos podem obter os dados relacionados ao recurso por meio do provedor de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="fcd93-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="fcd93-107">Você pode adicionar e modificar os recursos do sistema no registro.</span><span class="sxs-lookup"><span data-stu-id="fcd93-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="fcd93-108">O procedimento a seguir descreve como armazenar informações relacionadas ao recurso no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="fcd93-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="fcd93-109">**Para armazenar informações relacionadas ao recurso no registro do sistema**</span><span class="sxs-lookup"><span data-stu-id="fcd93-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="fcd93-110">Crie uma cadeia de caracteres que contenha os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="fcd93-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="fcd93-111">Campo</span><span class="sxs-lookup"><span data-stu-id="fcd93-111">Field</span></span></th>
    <th><span data-ttu-id="fcd93-112">Contém</span><span class="sxs-lookup"><span data-stu-id="fcd93-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="fcd93-113">Tipo de interface</span><span class="sxs-lookup"><span data-stu-id="fcd93-113">Interface type</span></span></td>
    <td><span data-ttu-id="fcd93-114">Um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fcd93-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="fcd93-115">Interna</span><span class="sxs-lookup"><span data-stu-id="fcd93-115">Internal</span></span><br />
    <span data-ttu-id="fcd93-116">ISA</span><span class="sxs-lookup"><span data-stu-id="fcd93-116">Isa</span></span><br />
    <span data-ttu-id="fcd93-117">EISA</span><span class="sxs-lookup"><span data-stu-id="fcd93-117">Eisa</span></span><br />
    <span data-ttu-id="fcd93-118">Microchannel</span><span class="sxs-lookup"><span data-stu-id="fcd93-118">MicroChannel</span></span><br />
    <span data-ttu-id="fcd93-119">TurboChannel</span><span class="sxs-lookup"><span data-stu-id="fcd93-119">TurboChannel</span></span><br />
    <span data-ttu-id="fcd93-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="fcd93-120">PCIBus</span></span><br />
    <span data-ttu-id="fcd93-121">VMEBus</span><span class="sxs-lookup"><span data-stu-id="fcd93-121">VMEBus</span></span><br />
    <span data-ttu-id="fcd93-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="fcd93-122">NuBus</span></span><br />
    <span data-ttu-id="fcd93-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="fcd93-123">PCMCIABus</span></span><br />
    <span data-ttu-id="fcd93-124">CBus</span><span class="sxs-lookup"><span data-stu-id="fcd93-124">CBus</span></span><br />
    <span data-ttu-id="fcd93-125">MPIBus</span><span class="sxs-lookup"><span data-stu-id="fcd93-125">MPIBus</span></span><br />
    <span data-ttu-id="fcd93-126">MPSABus</span><span class="sxs-lookup"><span data-stu-id="fcd93-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fcd93-127">Número do barramento</span><span class="sxs-lookup"><span data-stu-id="fcd93-127">Bus number</span></span></td>
    <td><span data-ttu-id="fcd93-128">Inteiro que especifica o número do barramento.</span><span class="sxs-lookup"><span data-stu-id="fcd93-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="fcd93-129">Número de descritor parcial</span><span class="sxs-lookup"><span data-stu-id="fcd93-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="fcd93-130">Inteiro que especifica o número do descritor.</span><span class="sxs-lookup"><span data-stu-id="fcd93-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fcd93-131">Tipo de deslocamento ou de União</span><span class="sxs-lookup"><span data-stu-id="fcd93-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="fcd93-132">Um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fcd93-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="fcd93-133">Port. Start</span><span class="sxs-lookup"><span data-stu-id="fcd93-133">Port.Start</span></span><br />
    <span data-ttu-id="fcd93-134">Port. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="fcd93-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="fcd93-135">Port. Length</span><span class="sxs-lookup"><span data-stu-id="fcd93-135">Port.Length</span></span><br />
    <span data-ttu-id="fcd93-136">Interrupção. nível</span><span class="sxs-lookup"><span data-stu-id="fcd93-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="fcd93-137">Interrupção. vetor</span><span class="sxs-lookup"><span data-stu-id="fcd93-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="fcd93-138">Interrupção. afinidade</span><span class="sxs-lookup"><span data-stu-id="fcd93-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="fcd93-139">Memória. iniciar</span><span class="sxs-lookup"><span data-stu-id="fcd93-139">Memory.Start</span></span><br />
    <span data-ttu-id="fcd93-140">Memória. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="fcd93-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="fcd93-141">Memória. comprimento</span><span class="sxs-lookup"><span data-stu-id="fcd93-141">Memory.Length</span></span><br />
    <span data-ttu-id="fcd93-142">DMA. Channel</span><span class="sxs-lookup"><span data-stu-id="fcd93-142">Dma.Channel</span></span><br />
    <span data-ttu-id="fcd93-143">DMA. porta</span><span class="sxs-lookup"><span data-stu-id="fcd93-143">Dma.Port</span></span><br />
    <span data-ttu-id="fcd93-144">DMA. Reserved1</span><span class="sxs-lookup"><span data-stu-id="fcd93-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="fcd93-145">DeviceSpecificData. DataSize</span><span class="sxs-lookup"><span data-stu-id="fcd93-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="fcd93-146">DeviceSpecificData. Reserved1</span><span class="sxs-lookup"><span data-stu-id="fcd93-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="fcd93-147">DeviceSpecificData. Reserved2</span><span class="sxs-lookup"><span data-stu-id="fcd93-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="fcd93-148">Coloque a cadeia de caracteres na chave apropriada sob a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="fcd93-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="fcd93-149">O exemplo de código a seguir descreve um descritor de recurso válido.</span><span class="sxs-lookup"><span data-stu-id="fcd93-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="fcd93-150">O exemplo de código a seguir mostra uma sintaxe MOF válida para recuperar um descritor de recurso.</span><span class="sxs-lookup"><span data-stu-id="fcd93-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




