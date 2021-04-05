---
title: SNB (Objidl. h)
description: Um bloco de nome de cadeia de caracteres (SNB) é um ponteiro para uma matriz de ponteiros para cadeias de caracteres, que termina em um ponteiro nulo.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918221"
---
# <a name="snb"></a><span data-ttu-id="02ee3-104">SNB</span><span class="sxs-lookup"><span data-stu-id="02ee3-104">SNB</span></span>

<span data-ttu-id="02ee3-105">Um bloco de nome de cadeia de caracteres (**SNB**) é um ponteiro para uma matriz de ponteiros para cadeias de caracteres, que termina em um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="02ee3-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="02ee3-106">Os blocos de nomes de cadeia de caracteres são usados pela interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e por chamadas de função que abrem objetos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="02ee3-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="02ee3-107">As cadeias de caracteres apontam para objetos de armazenamento contidos ou fluxos que devem ser excluídos nas chamadas abertas.</span><span class="sxs-lookup"><span data-stu-id="02ee3-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="02ee3-108">**SNB**</span><span class="sxs-lookup"><span data-stu-id="02ee3-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="02ee3-109">\[\_marshaling de conexão (wireSNB)\]</span><span class="sxs-lookup"><span data-stu-id="02ee3-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02ee3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="02ee3-110">Remarks</span></span>

<span data-ttu-id="02ee3-111">O **SNB** deve ser criado alocando um bloco contíguo de memória no qual os ponteiros para cadeias de caracteres são seguidos por um ponteiro **NULL** , que é seguido pelas cadeias de caracteres reais.</span><span class="sxs-lookup"><span data-stu-id="02ee3-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="02ee3-112">O marshaling de um **SNB** é baseado na suposição de que o **SNB** que foi passado foi criado dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="02ee3-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="02ee3-113">Embora possa ser armazenado de outras maneiras, o **SNB** criado dessa maneira tem a vantagem de exigir apenas uma operação de alocação e uma liberação de memória para todas as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02ee3-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ee3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02ee3-114">Requirements</span></span>



| <span data-ttu-id="02ee3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ee3-115">Requirement</span></span> | <span data-ttu-id="02ee3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="02ee3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02ee3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ee3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02ee3-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02ee3-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="02ee3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ee3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02ee3-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02ee3-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="02ee3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02ee3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ee3-122"><dt>Objidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ee3-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="02ee3-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="02ee3-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02ee3-124"><dt>Objidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02ee3-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ee3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="02ee3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ee3-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="02ee3-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





