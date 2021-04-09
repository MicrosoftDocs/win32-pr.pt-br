---
title: Estrutura de WINBIO_IDENTITY (WinBio \_ Types. h)
description: Contém um valor de identificação associado a um modelo biométrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_IDENTITY
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085661"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="4b40d-104">\_Estrutura de identidade WINBIO</span><span class="sxs-lookup"><span data-stu-id="4b40d-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="4b40d-105">A estrutura de **\_ identidade WINBIO** contém um valor de identificação associado a um modelo biométrico.</span><span class="sxs-lookup"><span data-stu-id="4b40d-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b40d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b40d-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="4b40d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4b40d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b40d-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4b40d-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-109">Especifica o formato das informações de identidade contidas nesta estrutura.</span><span class="sxs-lookup"><span data-stu-id="4b40d-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="4b40d-110">Esse valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4b40d-110">This can be one of the following values:</span></span>



| <span data-ttu-id="4b40d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4b40d-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="4b40d-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4b40d-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="4b40d-113"><dt>**\_tipo de ID WINBIO \_ \_ NULL**</dt></span><span class="sxs-lookup"><span data-stu-id="4b40d-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="4b40d-114">O modelo não tem nenhuma ID associada.</span><span class="sxs-lookup"><span data-stu-id="4b40d-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="4b40d-115"><dt>**\_tipo de ID WINBIO \_ \_ curinga**</dt></span><span class="sxs-lookup"><span data-stu-id="4b40d-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="4b40d-116">A estrutura corresponde a todas as identidades de modelo.</span><span class="sxs-lookup"><span data-stu-id="4b40d-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="4b40d-117"><dt>**\_GUID do \_ tipo de ID de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4b40d-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="4b40d-118">A estrutura contém um GUID associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="4b40d-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="4b40d-119"><dt>**\_SID do \_ tipo de ID de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4b40d-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="4b40d-120">A estrutura contém o SID da conta associado ao modelo.</span><span class="sxs-lookup"><span data-stu-id="4b40d-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4b40d-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4b40d-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-122">Uma União que pode conter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4b40d-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="4b40d-123">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="4b40d-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-124">Contém 1 se o membro do **tipo** for **WINBIO \_ ID \_ Type \_ NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b40d-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4b40d-125">**Amplia**</span><span class="sxs-lookup"><span data-stu-id="4b40d-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-126">Contém 1 se o membro de **tipo** for um **tipo de \_ ID WINBIO \_ \_ curinga**.</span><span class="sxs-lookup"><span data-stu-id="4b40d-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="4b40d-127">**TemplateGuid**</span><span class="sxs-lookup"><span data-stu-id="4b40d-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-128">Contém um valor de GUID de 128 bits que identifica o modelo se o membro de **tipo** for o **tipo de \_ ID WINBIO \_ \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="4b40d-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="4b40d-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="4b40d-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-130">Uma estrutura que contém um SID de conta se o membro do **tipo** for **WINBIO \_ ID do \_ tipo \_ Sid**.</span><span class="sxs-lookup"><span data-stu-id="4b40d-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="4b40d-131">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="4b40d-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-132">O número de caracteres no SID.</span><span class="sxs-lookup"><span data-stu-id="4b40d-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="4b40d-133">**Dados**</span><span class="sxs-lookup"><span data-stu-id="4b40d-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="4b40d-134">Uma matriz de caracteres não assinados que contêm o SID.</span><span class="sxs-lookup"><span data-stu-id="4b40d-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="4b40d-135">O tamanho máximo atual da matriz é de 68 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4b40d-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b40d-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b40d-136">Remarks</span></span>

<span data-ttu-id="4b40d-137">Essa estrutura é usada nas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="4b40d-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="4b40d-138">**WinBioDeleteTemplate**</span><span class="sxs-lookup"><span data-stu-id="4b40d-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="4b40d-139">**WinBioEnrollCommit**</span><span class="sxs-lookup"><span data-stu-id="4b40d-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="4b40d-140">**WinBioEnumEnrollments**</span><span class="sxs-lookup"><span data-stu-id="4b40d-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="4b40d-141">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="4b40d-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="4b40d-142">**WinBioIdentify**</span><span class="sxs-lookup"><span data-stu-id="4b40d-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="4b40d-143">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="4b40d-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="4b40d-144">**WinBioVerify**</span><span class="sxs-lookup"><span data-stu-id="4b40d-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="4b40d-145">**WinBioVerifyWithCallback**</span><span class="sxs-lookup"><span data-stu-id="4b40d-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="4b40d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b40d-146">Requirements</span></span>



| <span data-ttu-id="4b40d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b40d-147">Requirement</span></span> | <span data-ttu-id="4b40d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="4b40d-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b40d-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b40d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4b40d-150">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4b40d-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4b40d-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b40d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4b40d-152">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="4b40d-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4b40d-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b40d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b40d-154"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b40d-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b40d-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b40d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b40d-156">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="4b40d-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





