---
description: Cria uma matriz de identificadores para ícones extraídos de um arquivo especificado.
title: Função SHExtractIconsW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989014"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="c2f17-103">Função SHExtractIconsW</span><span class="sxs-lookup"><span data-stu-id="c2f17-103">SHExtractIconsW function</span></span>

<span data-ttu-id="c2f17-104">\[O **SHExtractIconsW** está disponível por meio do Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="c2f17-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="c2f17-105">Ele pode ser alterado ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c2f17-106">Cria uma matriz de identificadores para ícones extraídos de um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2f17-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f17-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2f17-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="c2f17-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2f17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f17-109">*pszFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c2f17-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c2f17-111">Um ponteiro para o nome de arquivo do qual extrair os ícones.</span><span class="sxs-lookup"><span data-stu-id="c2f17-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-112">*nIconIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c2f17-113">Type: **int**</span></span>

<span data-ttu-id="c2f17-114">O índice do primeiro ícone a ser extraído do recurso nomeado em *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="c2f17-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-115">*cxIcon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c2f17-116">Type: **int**</span></span>

<span data-ttu-id="c2f17-117">A largura desejada do ícone.</span><span class="sxs-lookup"><span data-stu-id="c2f17-117">The desired width of the icon.</span></span> <span data-ttu-id="c2f17-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="c2f17-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-119">*cyIcon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-120">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c2f17-120">Type: **int**</span></span>

<span data-ttu-id="c2f17-121">A altura desejada do ícone.</span><span class="sxs-lookup"><span data-stu-id="c2f17-121">The desired height of the icon.</span></span> <span data-ttu-id="c2f17-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="c2f17-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-123">*phIcon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-124">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="c2f17-124">Type: \**HICON\** _</span></span>

<span data-ttu-id="c2f17-125">Quando essa função retorna, contém um ponteiro para a matriz de alças de ícone.</span><span class="sxs-lookup"><span data-stu-id="c2f17-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-126">_pIconId \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-126">_pIconId\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-127">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c2f17-127">Type: \**UINT\** _</span></span>

<span data-ttu-id="c2f17-128">Quando essa função retorna, contém um ponteiro para o identificador de recurso do ícone extraído que melhor se adapta ao dispositivo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="c2f17-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="c2f17-129">Se não houver nenhum identificador disponível para esse formato, ele conterá 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c2f17-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="c2f17-130">Se nenhum identificador puder ser obtido por qualquer outro motivo, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c2f17-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-131">_nIcons \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-131">_nIcons\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c2f17-132">Type: **UINT**</span></span>

<span data-ttu-id="c2f17-133">O número de ícones a serem extraídos do recurso nomeado em *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="c2f17-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="c2f17-134">Esse parâmetro é válido somente quando o recurso é um arquivo. exe ou. dll.</span><span class="sxs-lookup"><span data-stu-id="c2f17-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="c2f17-135">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f17-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c2f17-136">Type: **UINT**</span></span>

<span data-ttu-id="c2f17-137">Os sinalizadores que controlam essa função.</span><span class="sxs-lookup"><span data-stu-id="c2f17-137">The flags that control this function.</span></span> <span data-ttu-id="c2f17-138">Para obter os valores possíveis, consulte o parâmetro *fuLoad* da função [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .</span><span class="sxs-lookup"><span data-stu-id="c2f17-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2f17-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2f17-139">Return value</span></span>

<span data-ttu-id="c2f17-140">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c2f17-140">Type: **UINT**</span></span>

<span data-ttu-id="c2f17-141">Um valor diferente de zero, se for bem-sucedido; caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="c2f17-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f17-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2f17-142">Remarks</span></span>

<span data-ttu-id="c2f17-143">**SHExtractIconsW** extrai dos seguintes tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2f17-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="c2f17-144">Executável (.exe)</span><span class="sxs-lookup"><span data-stu-id="c2f17-144">Executable (.exe)</span></span>
-   <span data-ttu-id="c2f17-145">DLL (. dll)</span><span class="sxs-lookup"><span data-stu-id="c2f17-145">DLL (.dll)</span></span>
-   <span data-ttu-id="c2f17-146">Ícone (. ico)</span><span class="sxs-lookup"><span data-stu-id="c2f17-146">Icon (.ico)</span></span>
-   <span data-ttu-id="c2f17-147">Cursor (. cur)</span><span class="sxs-lookup"><span data-stu-id="c2f17-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="c2f17-148">Cursor animado (. ani)</span><span class="sxs-lookup"><span data-stu-id="c2f17-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="c2f17-149">Bitmap (.bpm)</span><span class="sxs-lookup"><span data-stu-id="c2f17-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="c2f17-150">Extrações do Windows 3. também há suporte para arquivos executáveis *de 16 bits* (. exe ou. dll).</span><span class="sxs-lookup"><span data-stu-id="c2f17-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="c2f17-151">Os parâmetros *cxIcon* e *cyIcon* especificam o tamanho dos ícones a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="c2f17-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="c2f17-152">Dois tamanhos podem ser extraídos por meio de cada parâmetro, dividindo o valor entre seu LOWORD e HIWORD.</span><span class="sxs-lookup"><span data-stu-id="c2f17-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="c2f17-153">Coloque o primeiro tamanho desejado no LOWORD do parâmetro e o segundo tamanho no HIWORD.</span><span class="sxs-lookup"><span data-stu-id="c2f17-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="c2f17-154">Por exemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* e *cyIcon* extrai os ícones de tamanho 24 e 48.</span><span class="sxs-lookup"><span data-stu-id="c2f17-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="c2f17-155">O processo de chamada é responsável por destruir todos os ícones extraídos por essa função chamando a função [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .</span><span class="sxs-lookup"><span data-stu-id="c2f17-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="c2f17-156">**SHExtractIconsW** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="c2f17-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="c2f17-157">Para usá-lo, você deve declarar um protótipo correspondente e usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar um ponteiro de função de Shell32.dll que possa ser usado para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="c2f17-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f17-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f17-158">Requirements</span></span>



| <span data-ttu-id="c2f17-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f17-159">Requirement</span></span> | <span data-ttu-id="c2f17-160">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f17-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f17-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f17-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f17-162">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2f17-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f17-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f17-164">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2f17-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2f17-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f17-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f17-166"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c2f17-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="c2f17-167">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c2f17-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c2f17-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="c2f17-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
