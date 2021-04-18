---
description: Descreve uma regra para o acesso a itens armazenados no armazenamento protegido.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Estrutura de PST_ACCESSRULE (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749927"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="4e1fa-103">Estrutura de ACCESSRULE de PST \_</span><span class="sxs-lookup"><span data-stu-id="4e1fa-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="4e1fa-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4e1fa-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4e1fa-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4e1fa-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4e1fa-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4e1fa-108">Descreve uma regra para o acesso a itens armazenados no armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1fa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e1fa-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="4e1fa-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4e1fa-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e1fa-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="4e1fa-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e1fa-113">**AccessModeFlags**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4e1fa-114">Os modos de acesso aos quais o conjunto especificado de cláusulas de acesso pertence.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="4e1fa-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4e1fa-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="4e1fa-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4e1fa-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="4e1fa-117"><dt>**PST \_ LER**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="4e1fa-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="4e1fa-118">Modo de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="4e1fa-119"><dt>**PST \_**</dt> <dt>0X0002</dt> de gravação</span><span class="sxs-lookup"><span data-stu-id="4e1fa-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="4e1fa-120">Modo de acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="4e1fa-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e1fa-121">**cClauses**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="4e1fa-122">O número de estruturas na matriz **rgClauses** .</span><span class="sxs-lookup"><span data-stu-id="4e1fa-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="4e1fa-123">**rgClauses**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="4e1fa-124">Um ponteiro para uma matriz de [**estruturas \_ ACCESSCLAUSE de PST**](pst-accessclause.md) .</span><span class="sxs-lookup"><span data-stu-id="4e1fa-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e1fa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e1fa-125">Requirements</span></span>



| <span data-ttu-id="4e1fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e1fa-126">Requirement</span></span> | <span data-ttu-id="4e1fa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4e1fa-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1fa-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e1fa-128">Header</span></span><br/> | <dl> <span data-ttu-id="4e1fa-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1fa-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1fa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e1fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1fa-131">**\_ACCESSCLAUSE PST**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="4e1fa-132">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="4e1fa-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
