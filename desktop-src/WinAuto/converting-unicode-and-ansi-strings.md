---
title: Convertendo cadeias de caracteres Unicode e ANSI
description: O Microsoft Acessibilidade Ativa usa cadeias de caracteres Unicode, conforme definido pelo tipo de dados BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294276"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="6d076-103">Convertendo cadeias de caracteres Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6d076-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="6d076-104">O Microsoft Acessibilidade Ativa usa cadeias de caracteres Unicode, conforme definido pelo tipo de dados **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6d076-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="6d076-105">Se seu aplicativo não usar cadeias de caracteres Unicode ou se você quiser converter cadeias de caracteres para determinadas chamadas de API, use as funções do Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para executar a conversão necessária.</span><span class="sxs-lookup"><span data-stu-id="6d076-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="6d076-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para converter uma cadeia de caracteres Unicode em uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="6d076-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="6d076-107">A função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) converte uma cadeia de caracteres ANSI em uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6d076-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="6d076-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) para alocar e liberar tipos de dados **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6d076-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="6d076-109">Para obter mais informações sobre essas funções de cadeia de caracteres, consulte suas referências no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d076-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 