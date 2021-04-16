---
description: Enumera os membros do arquivo individual na seção CatalogFiles de um arquivo de definição de catálogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Função CryptCATCDFEnumMembersByCDFTagEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501549"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="ccfd3-103">Função CryptCATCDFEnumMembersByCDFTagEx</span><span class="sxs-lookup"><span data-stu-id="ccfd3-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="ccfd3-104">\[A função **CryptCATCDFEnumMembersByCDFTagEx** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ccfd3-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="ccfd3-106">A função **CryptCATCDFEnumMembersByCDFTagEx** enumera os membros de arquivo individuais na seção **CatalogFiles** de um arquivo de definição de catálogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="ccfd3-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="ccfd3-107">**CryptCATCDFEnumMembersByCDFTagEx** é chamado por [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="ccfd3-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="ccfd3-108">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="ccfd3-109">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ccfd3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccfd3-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="ccfd3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccfd3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccfd3-112">*pCDF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-113">Um ponteiro para uma estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="ccfd3-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ccfd3-114">*pwszPrevCDFTag* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-115">Um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica o membro do arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="ccfd3-116">*pfnParseError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-117">Um ponteiro para uma função definida pelo usuário para manipular erros de análise de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="ccfd3-118">*ppMember* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-119">Um ponteiro para uma estrutura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contém as informações de membro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="ccfd3-120">*fContinueOnError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-121">Um valor que especifica se a memória deve ser mantida em uma referência ao último membro enumerado.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="ccfd3-122">*pvReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccfd3-123">Este parâmetro é reservado; Não o use.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccfd3-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccfd3-124">Return value</span></span>

<span data-ttu-id="ccfd3-125">Após o êxito, essa função retorna um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica um membro de arquivo na seção **CATALOGFILES** de um CDF.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="ccfd3-126">A função **CryptCATCDFEnumMembersByCDFTagEx** retornará um ponteiro **nulo** se falhar.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccfd3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccfd3-127">Remarks</span></span>

<span data-ttu-id="ccfd3-128">Normalmente, você chama essa função em um loop para enumerar todos os membros do arquivo de catálogo em um CDF.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="ccfd3-129">Antes de entrar no loop, defina *pwszPrevCDFTag* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="ccfd3-130">A função retorna um ponteiro para o primeiro membro.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="ccfd3-131">Defina *pwszPrevCDFTag* como o valor de retorno da função para iterações subsequentes do loop.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="ccfd3-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccfd3-132">Examples</span></span>

<span data-ttu-id="ccfd3-133">O exemplo a seguir mostra a sequência correta de atribuições para o parâmetro *pwszPrevCDFTag* ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="ccfd3-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="ccfd3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccfd3-134">Requirements</span></span>



| <span data-ttu-id="ccfd3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccfd3-135">Requirement</span></span> | <span data-ttu-id="ccfd3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ccfd3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfd3-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccfd3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ccfd3-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ccfd3-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccfd3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ccfd3-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ccfd3-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ccfd3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ccfd3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccfd3-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccfd3-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccfd3-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccfd3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfd3-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="ccfd3-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="ccfd3-145">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="ccfd3-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="ccfd3-146">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="ccfd3-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="ccfd3-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="ccfd3-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="ccfd3-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="ccfd3-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
