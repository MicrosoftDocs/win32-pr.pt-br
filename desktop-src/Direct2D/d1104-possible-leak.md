---
title: D1104 Possível Vazamento
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: A fábrica foi liberada, mas a interface criada a partir dela ainda está a vivo. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode ser um indicativo de uma perda de memória.
keywords:
- D1104 Possível Vazamento Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548671"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="cfe1e-105">D1104: Possível vazamento</span><span class="sxs-lookup"><span data-stu-id="cfe1e-105">D1104: Possible Leak</span></span>

<span data-ttu-id="cfe1e-106">A fábrica \[ *de fábrica* \] foi lançada, mas a interface de \[ *interface* criada a partir dela \] ainda está a vivo.</span><span class="sxs-lookup"><span data-stu-id="cfe1e-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="cfe1e-107">Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode ser um indicativo de uma perda de memória.</span><span class="sxs-lookup"><span data-stu-id="cfe1e-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="cfe1e-108">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="cfe1e-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="cfe1e-109"><span id="factory"></span><span id="FACTORY"></span>*Fábrica*</span><span class="sxs-lookup"><span data-stu-id="cfe1e-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="cfe1e-110">O endereço da fábrica que foi liberada.</span><span class="sxs-lookup"><span data-stu-id="cfe1e-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="cfe1e-111"><span id="interface"></span><span id="INTERFACE"></span>*Interface*</span><span class="sxs-lookup"><span data-stu-id="cfe1e-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="cfe1e-112">O endereço da interface que foi criada na *fábrica.*</span><span class="sxs-lookup"><span data-stu-id="cfe1e-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="cfe1e-113">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="cfe1e-113">Error Level</span></span> | <span data-ttu-id="cfe1e-114">Informações</span><span class="sxs-lookup"><span data-stu-id="cfe1e-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="cfe1e-115">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="cfe1e-115">Possible Causes</span></span>

<span data-ttu-id="cfe1e-116">A fábrica foi liberada, mas a interface criada a partir dela ainda está a vivo.</span><span class="sxs-lookup"><span data-stu-id="cfe1e-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




