---
description: O tipo de dados LARGEINT define um \_ valor inteiro grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778538"
---
# <a name="largeint"></a><span data-ttu-id="ec95f-103">LARGEINT</span><span class="sxs-lookup"><span data-stu-id="ec95f-103">LARGEINT</span></span>

<span data-ttu-id="ec95f-104">O tipo de dados **LARGEINT** define um valor [**\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .</span><span class="sxs-lookup"><span data-stu-id="ec95f-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="ec95f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec95f-105">Remarks</span></span>

<span data-ttu-id="ec95f-106">O membro **lpLargeIntTable** da estrutura [**set**](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais valores LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="ec95f-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="ec95f-107">Quando esse tipo de estrutura de **conjunto** é especificado, monitor de rede exibe um dos seguintes rótulos com cada valor de LARGEINT que ele encontra no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ec95f-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="ec95f-108">Corresponde ao valor definido.</span><span class="sxs-lookup"><span data-stu-id="ec95f-108">Matches set value.</span></span> <span data-ttu-id="ec95f-109">O valor de LARGEINT é incluído no conjunto.</span><span class="sxs-lookup"><span data-stu-id="ec95f-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="ec95f-110">Valor de conjunto desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ec95f-110">Unknown set value.</span></span> <span data-ttu-id="ec95f-111">O valor de LARGEINT não está incluído no conjunto.</span><span class="sxs-lookup"><span data-stu-id="ec95f-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec95f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec95f-112">Requirements</span></span>



| <span data-ttu-id="ec95f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec95f-113">Requirement</span></span> | <span data-ttu-id="ec95f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ec95f-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec95f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec95f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec95f-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec95f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ec95f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec95f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec95f-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec95f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec95f-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec95f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec95f-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec95f-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec95f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec95f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec95f-122">SET</span><span class="sxs-lookup"><span data-stu-id="ec95f-122">SET</span></span>](set.md)
</dt> </dl>

 

