---
description: As classes a seguir são declaradas e associadas a identificadores de classe (CLSIDs) em wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificadores de classe para o analisador de Sumário (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758709"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="f4844-103">Identificadores de classe para o analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="f4844-104">As classes a seguir são declaradas e associadas a identificadores de classe (CLSIDs) em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f4844-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="f4844-105">Nome da classe</span><span class="sxs-lookup"><span data-stu-id="f4844-105">Class name</span></span>       | <span data-ttu-id="f4844-106">Nome amigável do objeto</span><span class="sxs-lookup"><span data-stu-id="f4844-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="f4844-107">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="f4844-107">CTocEntry</span></span>        | <span data-ttu-id="f4844-108">Entrada de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-108">TOC Entry</span></span>            |
| <span data-ttu-id="f4844-109">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="f4844-109">CTocEntryList</span></span>    | <span data-ttu-id="f4844-110">Lista de entradas de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-110">TOC Entry List</span></span>       |
| <span data-ttu-id="f4844-111">CToc</span><span class="sxs-lookup"><span data-stu-id="f4844-111">CToc</span></span>             | <span data-ttu-id="f4844-112">SUMÁRIO</span><span class="sxs-lookup"><span data-stu-id="f4844-112">TOC</span></span>                  |
| <span data-ttu-id="f4844-113">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="f4844-113">CTocCollection</span></span>   | <span data-ttu-id="f4844-114">Coleção de SUMÁRIOs</span><span class="sxs-lookup"><span data-stu-id="f4844-114">TOC Collection</span></span>       |
| <span data-ttu-id="f4844-115">CTocParser</span><span class="sxs-lookup"><span data-stu-id="f4844-115">CTocParser</span></span>       | <span data-ttu-id="f4844-116">Analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-116">TOC Parser</span></span>           |
| <span data-ttu-id="f4844-117">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="f4844-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="f4844-118">Gerador de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-118">TOC Generator</span></span>        |



 

<span data-ttu-id="f4844-119">A tabela anterior fornece um nome de objeto amigável para cada classe.</span><span class="sxs-lookup"><span data-stu-id="f4844-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="f4844-120">Esta documentação usa esses nomes amigáveis para se referir a instâncias das classes.</span><span class="sxs-lookup"><span data-stu-id="f4844-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="f4844-121">Por exemplo, a documentação refere-se a uma instância da classe CTocEntry como um objeto de entrada de Sumário.</span><span class="sxs-lookup"><span data-stu-id="f4844-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="f4844-122">No código, você pode usar **\_ \_ uuidof** para se referir aos CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="f4844-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="f4844-123">Por exemplo, você pode usar o código a seguir para se referir ao CLSID para CTocGeneratorDmo.</span><span class="sxs-lookup"><span data-stu-id="f4844-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="f4844-124">Constantes de CLSID definidas em Wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="f4844-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="f4844-125">Como alternativa ao uso de **\_ \_ uuidof**, você pode usar constantes para se referir aos CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="f4844-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="f4844-126">As constantes a seguir são definidas em wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="f4844-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="f4844-127">Nome da classe</span><span class="sxs-lookup"><span data-stu-id="f4844-127">Class name</span></span>     | <span data-ttu-id="f4844-128">Constante de CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="f4844-129">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="f4844-129">CTocEntry</span></span>      | <span data-ttu-id="f4844-130">\_CTOCENTRY CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="f4844-131">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="f4844-131">CTocEntryList</span></span>  | <span data-ttu-id="f4844-132">\_CTOCENTRYLIST CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="f4844-133">CToc</span><span class="sxs-lookup"><span data-stu-id="f4844-133">CToc</span></span>           | <span data-ttu-id="f4844-134">\_CTOC CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="f4844-135">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="f4844-135">CTocCollection</span></span> | <span data-ttu-id="f4844-136">\_CTOCCOLLECTION CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="f4844-137">CTocParser</span><span class="sxs-lookup"><span data-stu-id="f4844-137">CTocParser</span></span>     | <span data-ttu-id="f4844-138">\_CTOCPARSER CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="f4844-139">Constantes de CLSID definidas em Wmcodecdspuuid. lib</span><span class="sxs-lookup"><span data-stu-id="f4844-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="f4844-140">A constante de CLSID a seguir é declarada, mas não definida, em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f4844-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="f4844-141">Para usá-lo no código, você deve vincular a wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4844-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="f4844-142">Nome da classe</span><span class="sxs-lookup"><span data-stu-id="f4844-142">Class name</span></span>       | <span data-ttu-id="f4844-143">Constante de CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="f4844-144">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="f4844-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="f4844-145">\_CTOCGENERATORDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="f4844-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f4844-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4844-146">Requirements</span></span>



| <span data-ttu-id="f4844-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4844-147">Requirement</span></span> | <span data-ttu-id="f4844-148">Valor</span><span class="sxs-lookup"><span data-stu-id="f4844-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4844-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4844-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f4844-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4844-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4844-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4844-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f4844-152">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4844-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4844-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4844-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4844-154"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4844-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="f4844-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f4844-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4844-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4844-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f4844-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4844-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4844-158">Objetos do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="f4844-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




