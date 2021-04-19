---
description: Recupera os atributos básicos para o objeto de arquivo especificado.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Função NtQueryAttributesFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756512"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="4094c-103">Função NtQueryAttributesFile</span><span class="sxs-lookup"><span data-stu-id="4094c-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="4094c-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="4094c-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="4094c-105">Recupera os atributos básicos para o objeto de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4094c-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4094c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4094c-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="4094c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4094c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4094c-108">*Objetoattributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4094c-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4094c-109">Um ponteiro para uma estrutura de [ \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) que fornece os atributos a serem usados para o objeto de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4094c-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="4094c-110">*Informações* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4094c-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4094c-111">Um ponteiro para uma estrutura de [ \_ \_ informações básicas de arquivo](https://msdn.microsoft.com/library/aa491634.aspx) para receber as informações de atributo de arquivo retornado.</span><span class="sxs-lookup"><span data-stu-id="4094c-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4094c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4094c-112">Return value</span></span>

<span data-ttu-id="4094c-113">Retorna um NTSTATUS ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="4094c-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="4094c-114">Os formulários e o significado dos códigos de erro NTSTATUS são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="4094c-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4094c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4094c-115">Remarks</span></span>

<span data-ttu-id="4094c-116">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="4094c-116">This function has no associated header file.</span></span> <span data-ttu-id="4094c-117">A biblioteca de importação associada, ntdll. lib, está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="4094c-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="4094c-118">Você também pode usar as funções [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="4094c-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4094c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4094c-119">Requirements</span></span>



| <span data-ttu-id="4094c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4094c-120">Requirement</span></span> | <span data-ttu-id="4094c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4094c-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4094c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4094c-122">DLL</span></span><br/> | <dl> <span data-ttu-id="4094c-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4094c-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




