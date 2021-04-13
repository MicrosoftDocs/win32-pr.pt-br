---
title: Estrutura de WINBIO_BDB_ANSI_381_RECORD (WinBio \_ Types. h)
description: Contém informações sobre um único exemplo de impressão digital ou Palm de um usuário final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BDB_ANSI_381_RECORD
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369274"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="a6286-104">\_Estrutura de registro WINBIO BdB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="a6286-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="a6286-105">A estrutura de **\_ registro WINBIO BDB \_ ANSI \_ 381 \_** contém informações sobre um único exemplo de impressão digital ou Palm de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="a6286-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="a6286-106">Uma coleção dessas estruturas está incluída em cada estrutura [**de \_ cabeçalho WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .</span><span class="sxs-lookup"><span data-stu-id="a6286-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6286-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6286-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="a6286-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a6286-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6286-109">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="a6286-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-110">Contém o número de bytes nessa estrutura mais o número de bytes de dados de imagem de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a6286-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="a6286-111">**HorizontalLineLength**</span><span class="sxs-lookup"><span data-stu-id="a6286-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-112">Especifica o número de pixels em uma linha horizontal do exemplo.</span><span class="sxs-lookup"><span data-stu-id="a6286-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a6286-113">**VerticalLineLength**</span><span class="sxs-lookup"><span data-stu-id="a6286-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-114">Especifica o número de pixels em uma linha vertical do exemplo.</span><span class="sxs-lookup"><span data-stu-id="a6286-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a6286-115">**Posição**</span><span class="sxs-lookup"><span data-stu-id="a6286-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-116">Um valor de **\_ \_ subtipo biométrico WINBIO** que especifica o dedo ou o Palm usado para gerar o exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="a6286-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="a6286-117">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="a6286-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a6286-118">**CountOfViews**</span><span class="sxs-lookup"><span data-stu-id="a6286-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-119">Isso deve ser definido como um (1);</span><span class="sxs-lookup"><span data-stu-id="a6286-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="a6286-120">**ViewNumber**</span><span class="sxs-lookup"><span data-stu-id="a6286-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-121">Isso deve ser definido como um (1);</span><span class="sxs-lookup"><span data-stu-id="a6286-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="a6286-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="a6286-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a6286-123">Reserved.</span></span> <span data-ttu-id="a6286-124">Isso deve ser 254 (0xFE).</span><span class="sxs-lookup"><span data-stu-id="a6286-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="a6286-125">**Impressiontype**</span><span class="sxs-lookup"><span data-stu-id="a6286-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a6286-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a6286-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a6286-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a6286-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a6286-128">Reserved.</span></span> <span data-ttu-id="a6286-129">Deve ser definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="a6286-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6286-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6286-130">Remarks</span></span>

<span data-ttu-id="a6286-131">O membro de *posição* especifica a área da mão ou o Palm usado para criar o exemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="a6286-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="a6286-132">O Windows Biometric Framework (WBF) atualmente dá suporte apenas à captura de impressão digital e usa as constantes a seguir para representar informações de posição.</span><span class="sxs-lookup"><span data-stu-id="a6286-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="a6286-133">WINBIO \_ ANSI \_ 381 \_ pos \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="a6286-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="a6286-134">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="a6286-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="a6286-135">Dedo do índice de RH do WINBIO \_ ANSI \_ 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a6286-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="a6286-136">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ meio-dedo central de RH \_</span><span class="sxs-lookup"><span data-stu-id="a6286-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="a6286-137">WINBIO \_ ANSI \_ 381 \_ pos \_ - \_ anel de RH \_</span><span class="sxs-lookup"><span data-stu-id="a6286-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="a6286-138">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="a6286-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="a6286-139">WINBIO \_ ANSI \_ 381 \_ pos de \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="a6286-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="a6286-140">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="a6286-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="a6286-141">WINBIO \_ ANSI \_ 381 \_ pos \_ do \_ meio- \_ dedo médio</span><span class="sxs-lookup"><span data-stu-id="a6286-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="a6286-142">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Ring \_ Finger</span><span class="sxs-lookup"><span data-stu-id="a6286-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="a6286-143">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="a6286-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="a6286-144">WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="a6286-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="a6286-145">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="a6286-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="a6286-146">WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares</span><span class="sxs-lookup"><span data-stu-id="a6286-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a6286-147">Não tente validar o valor fornecido para o valor de *posição* .</span><span class="sxs-lookup"><span data-stu-id="a6286-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="a6286-148">O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação.</span><span class="sxs-lookup"><span data-stu-id="a6286-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="a6286-149">Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="a6286-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6286-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6286-150">Requirements</span></span>



| <span data-ttu-id="a6286-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6286-151">Requirement</span></span> | <span data-ttu-id="a6286-152">Valor</span><span class="sxs-lookup"><span data-stu-id="a6286-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6286-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6286-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a6286-154">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a6286-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a6286-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6286-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a6286-156">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a6286-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a6286-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6286-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6286-158"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6286-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6286-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6286-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6286-160">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="a6286-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





