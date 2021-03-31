---
title: Usando macros para tratamento de erro
description: COM define um número de macros que facilitam o trabalho com valores HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641880"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="a4a70-103">Usando macros para tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="a4a70-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="a4a70-104">COM define um número de macros que facilitam o trabalho com valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4a70-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="a4a70-105">As macros de tratamento de erros são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4a70-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4a70-106">Macro</span><span class="sxs-lookup"><span data-stu-id="a4a70-106">Macro</span></span></th>
<th><span data-ttu-id="a4a70-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4a70-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4a70-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-109">Retorna um <strong>HRESULT</strong> dado o bit de severidade, o código de recurso e o código de erro que compõem o <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a4a70-110">Chamar <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> para verificação de S_OK transporta uma penalidade de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a4a70-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="a4a70-111">Você não deve usar rotineiramente <strong>MAKE_HRESULT</strong> para resultados bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="a4a70-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-113">Retorna um <strong>SCODE</strong> dado o bit de severidade, o código de recurso e o código de erro que compõem o <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-115">Extrai a parte do código de erro do <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-117">Extrai o código de recurso do <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-119">Extrai o bit de severidade do <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-121">Extrai a parte do código de erro do <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-123">Extrai o código de recurso do <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-125">Extrai o campo de severidade do <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4a70-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>FOI</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-127">Testa o bit de severidade do <strong>SCODE</strong> ou <strong>HRESULT</strong>; retornará <strong>true</strong> se a severidade for zero e <strong>false</strong> se for uma.</span><span class="sxs-lookup"><span data-stu-id="a4a70-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>Falha ao</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-129">Testa o bit de severidade do <strong>SCODE</strong> ou <strong>HRESULT</strong>; retornará <strong>true</strong> se a severidade for um e <strong>false</strong> se for zero.</span><span class="sxs-lookup"><span data-stu-id="a4a70-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-131">Fornece um teste genérico para erros em qualquer valor de status.</span><span class="sxs-lookup"><span data-stu-id="a4a70-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4a70-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-133">Mapeia um <a href="/windows/desktop/Debug/system-error-codes">código de erro do sistema</a> para um valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4a70-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4a70-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4a70-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="a4a70-135">Mapeia um valor de status do NT para um valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4a70-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a4a70-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4a70-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a70-137">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="a4a70-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

