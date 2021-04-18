---
description: O método FindMediaFile procura um arquivo e, se for bem-sucedido, recupera o caminho para o arquivo.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Método IMediaLocator:: FindMediaFile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810174"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="6fd4a-103">Método IMediaLocator:: FindMediaFile</span><span class="sxs-lookup"><span data-stu-id="6fd4a-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="6fd4a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-104">\[Deprecated.</span></span> <span data-ttu-id="6fd4a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fd4a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fd4a-106">O `FindMediaFile` método procura um arquivo e, se for bem-sucedido, recupera o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd4a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fd4a-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="6fd4a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fd4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd4a-109">*Entrada*</span><span class="sxs-lookup"><span data-stu-id="6fd4a-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd4a-110">Nome do arquivo, incluindo o caminho, onde o arquivo foi conhecido pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="6fd4a-111">Para objetos de origem na linha do tempo, use o nome da mídia atual.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="6fd4a-112">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="6fd4a-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd4a-113">Um **BSTR** contendo pares de cadeias de caracteres de filtro, formatados conforme exigido pelo membro **LpstrFilter** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="6fd4a-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="6fd4a-114">O localizador de mídia usará esse filtro se ele exibir uma caixa de diálogo de abertura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="6fd4a-115">O valor pode ser **nulo** se o parâmetro *flags* não incluir o sinalizador de \_ \_ pop-up SFN VALIDATEF.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="6fd4a-116">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="6fd4a-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd4a-117">Ponteiro para uma variável que recebe o caminho real para o arquivo, se for diferente do valor contido na *entrada* e se o método localizar o arquivo com êxito.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="6fd4a-118">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="6fd4a-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd4a-119">Combinação de bits bit a zero ou mais sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="6fd4a-120">Para obter uma lista de possíveis sinalizadores, consulte [**sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6fd4a-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd4a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fd4a-121">Return value</span></span>

<span data-ttu-id="6fd4a-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fd4a-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fd4a-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd4a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fd4a-124">Remarks</span></span>

<span data-ttu-id="6fd4a-125">A cadeia de caracteres de filtro para a caixa de diálogo de abertura de arquivo, que é especificada pelo parâmetro *FilterString* , contém caracteres nulos internos.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="6fd4a-126">Por exemplo, \\ o vídeo 0 \* . avi \\ 0 \\ 0 é uma cadeia de caracteres de filtro válida.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="6fd4a-127">Você não pode usar a função **SysAllocStr** para alocar o BSTR, pois essa função espera uma cadeia de caracteres terminada em nulo e truncará a cadeia de caracteres no primeiro caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="6fd4a-128">Portanto, use uma função como **SysAllocStringLen**, que inclui um parâmetro explícito para o comprimento:</span><span class="sxs-lookup"><span data-stu-id="6fd4a-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="6fd4a-129">Se o usuário cancelar a caixa de diálogo de abertura de arquivo, o método retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="6fd4a-130">O método aloca memória para o **BSTR** em *pOutput*.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="6fd4a-131">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="6fd4a-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fd4a-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fd4a-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fd4a-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6fd4a-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fd4a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd4a-135">Requirements</span></span>



| <span data-ttu-id="6fd4a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd4a-136">Requirement</span></span> | <span data-ttu-id="6fd4a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6fd4a-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd4a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fd4a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="6fd4a-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd4a-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fd4a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fd4a-140">Library</span></span><br/> | <dl> <span data-ttu-id="6fd4a-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fd4a-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd4a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fd4a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd4a-143">**Interface IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="6fd4a-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="6fd4a-144">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6fd4a-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
