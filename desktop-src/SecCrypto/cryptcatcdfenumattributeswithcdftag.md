---
description: Enumera os atributos dos arquivos de membro na seção CatalogFiles de um arquivo de definição de catálogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Função CryptCATCDFEnumAttributesWithCDFTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501548"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="c0548-103">Função CryptCATCDFEnumAttributesWithCDFTag</span><span class="sxs-lookup"><span data-stu-id="c0548-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="c0548-104">\[A função **CryptCATCDFEnumAttributesWithCDFTag** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c0548-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c0548-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="c0548-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c0548-106">A função **CryptCATCDFEnumAttributesWithCDFTag** enumera os atributos dos arquivos de membro na seção **CatalogFiles** de um arquivo de definição de catálogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="c0548-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="c0548-107">**CryptCATCDFEnumAttributesWithCDFTag** é chamado por [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="c0548-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="c0548-108">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="c0548-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="c0548-109">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="c0548-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c0548-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0548-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="c0548-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0548-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0548-112">*pCDF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0548-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0548-113">Um ponteiro para uma estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="c0548-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0548-114">*pwszMemberTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0548-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0548-115">Um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica o membro do arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c0548-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="c0548-116">*pMember* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0548-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0548-117">Um ponteiro para uma estrutura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contém as informações do membro.</span><span class="sxs-lookup"><span data-stu-id="c0548-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="c0548-118">*pPrevAttr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0548-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0548-119">Um ponteiro para uma estrutura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) para um atributo de membro de arquivo no CDF apontado por *pCDF*.</span><span class="sxs-lookup"><span data-stu-id="c0548-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="c0548-120">*pfnParseError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0548-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0548-121">Um ponteiro para uma função definida pelo usuário para manipular erros de análise de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0548-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0548-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0548-122">Return value</span></span>

<span data-ttu-id="c0548-123">Após o êxito, essa função retorna um ponteiro para uma estrutura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) .</span><span class="sxs-lookup"><span data-stu-id="c0548-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="c0548-124">A função **CryptCATCDFEnumAttributesWithCDFTag** retornará um ponteiro **nulo** se falhar.</span><span class="sxs-lookup"><span data-stu-id="c0548-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0548-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0548-125">Remarks</span></span>

<span data-ttu-id="c0548-126">Normalmente, você chama essa função em um loop para enumerar todos os atributos de membro de arquivo de catálogo em um CDF.</span><span class="sxs-lookup"><span data-stu-id="c0548-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="c0548-127">Antes de entrar no loop, defina *pPrevAttr* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c0548-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="c0548-128">A função retorna um ponteiro para o primeiro atributo.</span><span class="sxs-lookup"><span data-stu-id="c0548-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="c0548-129">Defina *pPrevAttr* como o valor de retorno da função para iterações subsequentes do loop.</span><span class="sxs-lookup"><span data-stu-id="c0548-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="c0548-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0548-130">Examples</span></span>

<span data-ttu-id="c0548-131">O exemplo a seguir mostra a sequência correta de atribuições para o parâmetro *pPrevAttr* ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="c0548-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="c0548-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0548-132">Requirements</span></span>



| <span data-ttu-id="c0548-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0548-133">Requirement</span></span> | <span data-ttu-id="c0548-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c0548-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0548-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0548-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c0548-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c0548-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c0548-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0548-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c0548-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0548-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0548-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c0548-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0548-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0548-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0548-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0548-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0548-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="c0548-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="c0548-143">**CRYPTCATATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="c0548-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="c0548-144">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="c0548-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="c0548-145">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="c0548-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="c0548-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c0548-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="c0548-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="c0548-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
