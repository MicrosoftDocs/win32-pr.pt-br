---
description: Estima o risco de executar um código desconhecido quando um manipulador é chamado em um determinado arquivo. Esse risco se baseia em uma compreensão do manipulador e do conteúdo do código do arquivo.
title: Função EstimateFileRiskLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841427"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="ad71b-104">Função EstimateFileRiskLevel</span><span class="sxs-lookup"><span data-stu-id="ad71b-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="ad71b-105">\[Essa função está disponível no Windows XP com Service Pack 2 (SP2) por meio do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ad71b-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="ad71b-106">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="ad71b-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="ad71b-107">Em vez disso, os aplicativos cliente devem usar o [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) para apresentar um ambiente de usuário que fornece download seguro e troca de arquivos por email e anexos de mensagens.\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="ad71b-108">Estima o risco de executar um código desconhecido quando um manipulador é chamado em um determinado arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad71b-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="ad71b-109">Esse risco se baseia em uma compreensão do manipulador e do conteúdo do código do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad71b-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad71b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad71b-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="ad71b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad71b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad71b-112">*pszFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad71b-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ad71b-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ad71b-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho do arquivo que está sendo verificado em relação ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="ad71b-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="ad71b-115">*pszExt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad71b-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ad71b-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ad71b-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém a extensão do arquivo que está sendo verificado, seja com ou sem seu ponto principal.</span><span class="sxs-lookup"><span data-stu-id="ad71b-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="ad71b-118">Por exemplo, ". txt" ou "txt".</span><span class="sxs-lookup"><span data-stu-id="ad71b-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="ad71b-119">*pszHandler* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad71b-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ad71b-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ad71b-121">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho do manipulador para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad71b-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="ad71b-122">*pfrlEstimate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad71b-123">Tipo: **FILE \_ RISK \_ LEVEL \***</span><span class="sxs-lookup"><span data-stu-id="ad71b-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="ad71b-124">Quando essa função retorna com êxito, contém um ponteiro para um dos valores a seguir que afirmam o risco estimado.</span><span class="sxs-lookup"><span data-stu-id="ad71b-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="ad71b-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ NENHUMA \_ OPINIÃO** (0)</span><span class="sxs-lookup"><span data-stu-id="ad71b-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad71b-126">O formato do arquivo não é identificado ou o manipulador não é identificado.</span><span class="sxs-lookup"><span data-stu-id="ad71b-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="ad71b-127">Informações insuficientes disponíveis para uma resposta significativa.</span><span class="sxs-lookup"><span data-stu-id="ad71b-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="ad71b-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)</span><span class="sxs-lookup"><span data-stu-id="ad71b-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad71b-129">O formato do arquivo é completamente compreendido, o manipulador é conhecido e há alta confiança de que nenhum código não será executado.</span><span class="sxs-lookup"><span data-stu-id="ad71b-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="ad71b-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERADO** (2)</span><span class="sxs-lookup"><span data-stu-id="ad71b-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ad71b-131">O formato do arquivo é identificado, mas não é suficientemente compreendido para rotular como um risco alto ou baixo.</span><span class="sxs-lookup"><span data-stu-id="ad71b-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="ad71b-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTO** (3)</span><span class="sxs-lookup"><span data-stu-id="ad71b-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ad71b-133">O formato do arquivo é compreendido e fatores de risco elevados foram identificados.</span><span class="sxs-lookup"><span data-stu-id="ad71b-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="ad71b-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)</span><span class="sxs-lookup"><span data-stu-id="ad71b-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ad71b-135">O formato de arquivo é bloqueado especificamente para esse manipulador.</span><span class="sxs-lookup"><span data-stu-id="ad71b-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad71b-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad71b-136">Return value</span></span>

<span data-ttu-id="ad71b-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad71b-137">Type: **HRESULT**</span></span>

<span data-ttu-id="ad71b-138">Se essa função for bem-sucedida, ela **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="ad71b-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad71b-139">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ad71b-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad71b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad71b-140">Remarks</span></span>

<span data-ttu-id="ad71b-141">Essa função não é declarada em um header público nem incluída em um arquivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ad71b-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="ad71b-142">Para usá-lo, você deve carregá-lo diretamente Winshfhc.dll pelo ordinal 101.</span><span class="sxs-lookup"><span data-stu-id="ad71b-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad71b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad71b-143">Requirements</span></span>



| <span data-ttu-id="ad71b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad71b-144">Requirement</span></span> | <span data-ttu-id="ad71b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ad71b-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad71b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad71b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ad71b-147">Windows XP somente com aplicativos da \[ área de trabalho SP2\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad71b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad71b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ad71b-149">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad71b-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad71b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ad71b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad71b-151"><dt>Winshfhc.dll (versão 5,1 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ad71b-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




