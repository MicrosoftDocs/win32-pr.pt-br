---
description: Cria um certificado de usuário para uso com a conferência do NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Função NmMakeCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748691"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="003ff-103">Função NmMakeCert</span><span class="sxs-lookup"><span data-stu-id="003ff-103">NmMakeCert function</span></span>

<span data-ttu-id="003ff-104">Cria um certificado de usuário para uso com a conferência do NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="003ff-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="003ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="003ff-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="003ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="003ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003ff-107">*szFirstName*</span><span class="sxs-lookup"><span data-stu-id="003ff-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-108">O nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="003ff-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="003ff-109">*szLastName*</span><span class="sxs-lookup"><span data-stu-id="003ff-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-110">O sobrenome do usuário.</span><span class="sxs-lookup"><span data-stu-id="003ff-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="003ff-111">*szEmailName*</span><span class="sxs-lookup"><span data-stu-id="003ff-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-112">O nome de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="003ff-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="003ff-113">*szCity*</span><span class="sxs-lookup"><span data-stu-id="003ff-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-114">a cidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="003ff-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="003ff-115">*szCountry*</span><span class="sxs-lookup"><span data-stu-id="003ff-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-116">O país/região do usuário.</span><span class="sxs-lookup"><span data-stu-id="003ff-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="003ff-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="003ff-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="003ff-118">Um valor que indica como o certificado deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="003ff-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="003ff-119">Os valores podem ser qualquer um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="003ff-119">Values can be any of the following.</span></span>



| <span data-ttu-id="003ff-120">Valor</span><span class="sxs-lookup"><span data-stu-id="003ff-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="003ff-121">Significado</span><span class="sxs-lookup"><span data-stu-id="003ff-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="003ff-122"><dt>**NMMKCERT \_ \_ \_ Somente limpeza de F somente**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="003ff-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="003ff-123">Exclua o certificado antigo sem criar um novo.</span><span class="sxs-lookup"><span data-stu-id="003ff-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="003ff-124"><dt>**NMMKCERT \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="003ff-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="003ff-125">Exclua o certificado antigo criado anteriormente com essa função.</span><span class="sxs-lookup"><span data-stu-id="003ff-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="003ff-126"><dt>**NMMKCERT \_ F \_ \_ computador local**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="003ff-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="003ff-127">Crie o certificado no repositório de certificados do computador local.</span><span class="sxs-lookup"><span data-stu-id="003ff-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003ff-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="003ff-128">Return value</span></span>

<span data-ttu-id="003ff-129">Retornará 1 se a função for bem-sucedida e – 1 se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="003ff-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="003ff-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="003ff-130">Remarks</span></span>

<span data-ttu-id="003ff-131">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="003ff-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="003ff-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="003ff-132">Requirements</span></span>



| <span data-ttu-id="003ff-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="003ff-133">Requirement</span></span> | <span data-ttu-id="003ff-134">Valor</span><span class="sxs-lookup"><span data-stu-id="003ff-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="003ff-135">DLL</span><span class="sxs-lookup"><span data-stu-id="003ff-135">DLL</span></span><br/> | <dl> <span data-ttu-id="003ff-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="003ff-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
