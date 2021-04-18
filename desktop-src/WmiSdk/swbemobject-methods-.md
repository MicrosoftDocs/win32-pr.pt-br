---
description: A propriedade Methods \_ do objeto SWbemObject retorna um objeto SWbemMethodSet que é uma coleção de métodos para a classe ou instância atual. Esta propriedade é somente para leitura.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Methods_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797625"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="0587e-104">Propriedade SWbemObject. Methods \_</span><span class="sxs-lookup"><span data-stu-id="0587e-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="0587e-105">A **propriedade \_ Methods** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemMethodSet**](swbemmethodset.md) que é uma coleção de métodos para a classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="0587e-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="0587e-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0587e-106">This property is read-only.</span></span>

<span data-ttu-id="0587e-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0587e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0587e-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0587e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0587e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0587e-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="0587e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0587e-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="0587e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0587e-111">Examples</span></span>

<span data-ttu-id="0587e-112">O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)a seguir, extraído da galeria do TechNet, descreve como listar todos os métodos de uma classe.</span><span class="sxs-lookup"><span data-stu-id="0587e-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="0587e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0587e-113">Requirements</span></span>



| <span data-ttu-id="0587e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0587e-114">Requirement</span></span> | <span data-ttu-id="0587e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0587e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0587e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0587e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0587e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0587e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0587e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0587e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0587e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0587e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0587e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0587e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0587e-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0587e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0587e-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0587e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0587e-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0587e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0587e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0587e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0587e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0587e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0587e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="0587e-126">CLSID</span></span><br/>                    | <span data-ttu-id="0587e-127">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="0587e-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0587e-128">IID</span><span class="sxs-lookup"><span data-stu-id="0587e-128">IID</span></span><br/>                      | <span data-ttu-id="0587e-129">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="0587e-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




