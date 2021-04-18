---
title: Estrutura de WINBIO_BIR (WinBio \_ Types. h)
description: Representa um BIR (registro de informações biométricas).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770462"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="9fb76-104">\_Estrutura WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="9fb76-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="9fb76-105">A estrutura **WINBIO \_ Bir** representa um Bir (registro de informações biométricas).</span><span class="sxs-lookup"><span data-stu-id="9fb76-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="9fb76-106">O registro de informações contém cabeçalho, dados e blocos de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9fb76-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb76-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fb76-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="9fb76-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9fb76-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9fb76-109">**HeaderBlock**</span><span class="sxs-lookup"><span data-stu-id="9fb76-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="9fb76-110">Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento do cabeçalho Bir.</span><span class="sxs-lookup"><span data-stu-id="9fb76-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="9fb76-111">O cabeçalho contém informações que descrevem o conteúdo do registro de informações.</span><span class="sxs-lookup"><span data-stu-id="9fb76-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="9fb76-112">**StandardDataBlock**</span><span class="sxs-lookup"><span data-stu-id="9fb76-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="9fb76-113">Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento de informações biométricas processadas ou não processados criadas pelo Windows Biometric Framework (WBF).</span><span class="sxs-lookup"><span data-stu-id="9fb76-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="9fb76-114">**VendorDataBlock**</span><span class="sxs-lookup"><span data-stu-id="9fb76-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="9fb76-115">Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento de informações biométricas processadas ou não processados fornecidas por software e sensores do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9fb76-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="9fb76-116">**SignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="9fb76-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="9fb76-117">Uma estrutura [**de \_ \_ dados WINBIO Bir**](winbio-bir-data.md) opcional que contém o tamanho, em bytes, e o deslocamento do Mac (código de autenticação de mensagem de assinatura digital) que pode ser usado para verificar a integridade do Bir.</span><span class="sxs-lookup"><span data-stu-id="9fb76-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="9fb76-118">Se presente, a assinatura ou o MAC deve abranger o cabeçalho e os blocos de dados.</span><span class="sxs-lookup"><span data-stu-id="9fb76-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fb76-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fb76-119">Remarks</span></span>

<span data-ttu-id="9fb76-120">O uso de deslocamentos em vez de ponteiros permite uma fácil serialização do BIR e para uma tradução menos complicada entre os ambientes de 32 e 64 bits ou entre o modo de usuário e kernel.</span><span class="sxs-lookup"><span data-stu-id="9fb76-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="9fb76-121">O BIR é compatível com a CBEFF (estrutura de formato de intercâmbio biométrico) comum definida pelo NIST 6529-A.</span><span class="sxs-lookup"><span data-stu-id="9fb76-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="9fb76-122">Se essa estrutura contiver um valor *StandardDataBlock* , o parâmetro de *tipo* do cabeçalho especificado pelo parâmetro *HeaderBlock* deverá ser definido como **WINBIO \_ \_ \_ \_ tipo de formato ANSI 381**.</span><span class="sxs-lookup"><span data-stu-id="9fb76-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="9fb76-123">Esse é o único formato de dados padrão com suporte da versão atual do Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="9fb76-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb76-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb76-124">Requirements</span></span>



| <span data-ttu-id="9fb76-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb76-125">Requirement</span></span> | <span data-ttu-id="9fb76-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb76-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb76-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb76-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb76-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9fb76-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9fb76-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb76-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb76-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="9fb76-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9fb76-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fb76-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fb76-132"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fb76-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb76-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb76-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb76-134">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="9fb76-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="9fb76-135">**WINBIO \_ Bir \_ Data**</span><span class="sxs-lookup"><span data-stu-id="9fb76-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="9fb76-136">**\_cabeçalho WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="9fb76-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





