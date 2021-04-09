---
title: Estrutura de STOWED_EXCEPTION_INFORMATION_HEADER
description: Contém informações que identificam a estrutura pai.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Estrutura de STOWED_EXCEPTION_INFORMATION_HEADER Relatório de Erros do Windows
- Ponteiro de estrutura de PSTOWED_EXCEPTION_INFORMATION_HEADER Relatório de Erros do Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009676"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="32860-105">Estrutura de \_ \_ cabeçalho de informações de exceção dedevida \_</span><span class="sxs-lookup"><span data-stu-id="32860-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="32860-106">Contém informações que identificam a estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="32860-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="32860-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32860-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="32860-108">Membros</span><span class="sxs-lookup"><span data-stu-id="32860-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="32860-109">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="32860-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="32860-110">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="32860-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="32860-111">Tamanho, em bytes, da estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="32860-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="32860-112">**Signature**</span><span class="sxs-lookup"><span data-stu-id="32860-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="32860-113">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="32860-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="32860-114">Um valor de 32 bits que especifica a assinatura da estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="32860-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="32860-115">Valor</span><span class="sxs-lookup"><span data-stu-id="32860-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="32860-116">Significado</span><span class="sxs-lookup"><span data-stu-id="32860-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="32860-117">Em <dt>**DEdevido \_ \_Informações de \_ exceção \_ assinatura v1**</dt> <dt>' SE01 '</dt></span><span class="sxs-lookup"><span data-stu-id="32860-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="32860-118">Esse valor indica que o pai é uma estrutura de informações de exceção de nível **\_ \_ \_ v1** .</span><span class="sxs-lookup"><span data-stu-id="32860-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="32860-119">Em <dt>**DEdevido \_ \_ \_ \_ Assinatura de informações de exceção v2**</dt> <dt>' SE02 '</dt></span><span class="sxs-lookup"><span data-stu-id="32860-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="32860-120">Esse valor indica que o pai é uma estrutura de [**\_ \_ informações de \_ exceção dedevida**](stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="32860-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32860-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="32860-121">Remarks</span></span>

<span data-ttu-id="32860-122">Em [**DEdevido \_ \_As informações \_ de exceção v2**](stowed-exception-information-v2.md) e o **cabeçalho de \_ \_ informações \_ de exceção dedevida** não são definidas atualmente em um cabeçalho disponível publicamente, portanto, você precisa defini-las no código-fonte antes de usá-las.</span><span class="sxs-lookup"><span data-stu-id="32860-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="32860-123">A estrutura de informações de exceção devidada **\_ \_ \_ v1** é idêntica a essa estrutura, exceto que ela não contém os membros **NestedExceptionType** e **aninhaexception** .</span><span class="sxs-lookup"><span data-stu-id="32860-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="32860-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32860-124">Requirements</span></span>



| <span data-ttu-id="32860-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="32860-125">Requirement</span></span> | <span data-ttu-id="32860-126">Valor</span><span class="sxs-lookup"><span data-stu-id="32860-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="32860-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32860-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32860-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="32860-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="32860-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32860-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32860-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="32860-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="32860-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32860-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="32860-132"><dt>Nenhuma</dt></span><span class="sxs-lookup"><span data-stu-id="32860-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32860-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="32860-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32860-134">**Informações de exceção dedevidas \_ \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="32860-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

