---
description: Identifica o conjunto de regras de acesso para os dados de armazenamento protegido.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Estrutura de PST_ACCESSRULESET (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769135"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="709f4-103">Estrutura de ACCESSRULESET de PST \_</span><span class="sxs-lookup"><span data-stu-id="709f4-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="709f4-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="709f4-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="709f4-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="709f4-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="709f4-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="709f4-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="709f4-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="709f4-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="709f4-108">Identifica o conjunto de regras de acesso para os dados de armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="709f4-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="709f4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="709f4-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="709f4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="709f4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="709f4-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="709f4-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="709f4-112">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="709f4-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="709f4-113">**cRules**</span><span class="sxs-lookup"><span data-stu-id="709f4-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="709f4-114">O número de regras na matriz **rgRules** .</span><span class="sxs-lookup"><span data-stu-id="709f4-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="709f4-115">**rgRules**</span><span class="sxs-lookup"><span data-stu-id="709f4-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="709f4-116">Um ponteiro para uma matriz de [**estruturas \_ ACCESSRULE de PST**](pst-accessrule.md) .</span><span class="sxs-lookup"><span data-stu-id="709f4-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="709f4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="709f4-117">Requirements</span></span>



| <span data-ttu-id="709f4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="709f4-118">Requirement</span></span> | <span data-ttu-id="709f4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="709f4-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="709f4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="709f4-120">Header</span></span><br/> | <dl> <span data-ttu-id="709f4-121"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="709f4-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709f4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="709f4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709f4-123">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="709f4-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="709f4-124">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="709f4-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
