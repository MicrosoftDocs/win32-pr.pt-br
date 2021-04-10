---
title: D1104 possível perda
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa. Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode indicar um vazamento de memória.
keywords:
- D1104 possível Direct2D de vazamento
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293078"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="53525-105">D1104: possível vazamento</span><span class="sxs-lookup"><span data-stu-id="53525-105">D1104: Possible Leak</span></span>

<span data-ttu-id="53525-106">A fábrica de fábrica \[  \] foi liberada, mas a \[ *interface* \] de interface criada a partir dela ainda está ativa.</span><span class="sxs-lookup"><span data-stu-id="53525-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="53525-107">Embora seja válido liberar recursos depois de liberar a fábrica, essa condição pode indicar um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="53525-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="53525-108">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="53525-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="53525-109"><span id="factory"></span><span id="FACTORY"></span>*padrões*</span><span class="sxs-lookup"><span data-stu-id="53525-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="53525-110">O endereço da fábrica que foi lançada.</span><span class="sxs-lookup"><span data-stu-id="53525-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="53525-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="53525-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="53525-112">O endereço da interface que foi criada na *fábrica*.</span><span class="sxs-lookup"><span data-stu-id="53525-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="53525-113">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="53525-113">Error Level</span></span> | <span data-ttu-id="53525-114">Informações do</span><span class="sxs-lookup"><span data-stu-id="53525-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="53525-115">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="53525-115">Possible Causes</span></span>

<span data-ttu-id="53525-116">A fábrica foi liberada, mas a interface criada a partir dela ainda está ativa.</span><span class="sxs-lookup"><span data-stu-id="53525-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




