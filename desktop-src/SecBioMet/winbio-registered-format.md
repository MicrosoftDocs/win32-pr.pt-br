---
title: Estrutura de WINBIO_REGISTERED_FORMAT (WinBio \_ Types. h)
description: Especifica um formato de dados registrado como um par de proprietário/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_REGISTERED_FORMAT
- Ponteiro de estrutura de PWINBIO_REGISTERED_FORMAT Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499384"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="f0056-105">\_Estrutura de formato registrada WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f0056-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="f0056-106">A estrutura de **\_ \_ formato registrada WINBIO** especifica um formato de dados registrado como um par de proprietário/formato.</span><span class="sxs-lookup"><span data-stu-id="f0056-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0056-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0056-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="f0056-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f0056-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0056-109">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="f0056-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="f0056-110">Um valor de proprietário atribuído do IBIA (International biometricity Industry).</span><span class="sxs-lookup"><span data-stu-id="f0056-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="f0056-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0056-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f0056-112">Um formato atribuído pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="f0056-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0056-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0056-113">Remarks</span></span>

<span data-ttu-id="f0056-114">Como o Windows atualmente dá suporte apenas a leitores de impressão digital, os valores a seguir devem ser usados na estrutura de **\_ \_ formato registrada WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="f0056-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="f0056-115">Constante</span><span class="sxs-lookup"><span data-stu-id="f0056-115">Constant</span></span>                                    | <span data-ttu-id="f0056-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f0056-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0056-117">\_Proprietário do \_ formato ANSI 381 \_ \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="f0056-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="f0056-118">Comitê Internacional de INCITS (biometria) do Comitê Técnico de normas de tecnologia da informação (biométrica).</span><span class="sxs-lookup"><span data-stu-id="f0056-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="f0056-119">\_Tipo de formato WINBIO ANSI \_ 381 \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0056-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="f0056-120">Formato de intercâmbio de dados baseado em imagem de dedo ANSI INCITS 381.</span><span class="sxs-lookup"><span data-stu-id="f0056-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="f0056-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0056-121">Requirements</span></span>



| <span data-ttu-id="f0056-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0056-122">Requirement</span></span> | <span data-ttu-id="f0056-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f0056-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0056-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0056-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0056-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f0056-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f0056-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0056-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0056-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f0056-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f0056-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0056-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0056-129"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0056-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0056-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0056-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0056-131">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="f0056-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="f0056-132">**\_Constantes de formato WINBIO ANSI \_ 381 \_**</span><span class="sxs-lookup"><span data-stu-id="f0056-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="f0056-133">**\_Cabeçalho WINBIO BdB \_ ANSI \_ 381 \_**</span><span class="sxs-lookup"><span data-stu-id="f0056-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="f0056-134">**\_cabeçalho WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="f0056-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





