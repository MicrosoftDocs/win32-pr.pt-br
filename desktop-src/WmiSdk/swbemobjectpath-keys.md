---
description: A propriedade Keys do objeto SWbemObjectPath é um objeto SWbemNamedValueSet que contém as associações de valor de chave. Esta propriedade é somente para leitura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010761"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="29a31-104">Propriedade SWbemObjectPath. Keys</span><span class="sxs-lookup"><span data-stu-id="29a31-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="29a31-105">A propriedade **Keys** do objeto [**SWbemObjectPath**](swbemobjectpath.md) é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contém as associações de valor de chave.</span><span class="sxs-lookup"><span data-stu-id="29a31-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="29a31-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="29a31-106">This property is read-only.</span></span>

<span data-ttu-id="29a31-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="29a31-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="29a31-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="29a31-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a31-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29a31-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="29a31-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="29a31-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="29a31-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="29a31-111">Error codes</span></span>

<span data-ttu-id="29a31-112">Depois de recuperar a propriedade **Keys** , o objeto **Err** pode conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="29a31-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="29a31-113">**wbemErrNotSupported** -2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="29a31-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="29a31-114">Não há suporte para o recurso ou operação.</span><span class="sxs-lookup"><span data-stu-id="29a31-114">The feature or operation is not supported.</span></span> <span data-ttu-id="29a31-115">Esse erro será retornado se um script tentar gravar nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="29a31-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29a31-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29a31-116">Requirements</span></span>



| <span data-ttu-id="29a31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29a31-117">Requirement</span></span> | <span data-ttu-id="29a31-118">Valor</span><span class="sxs-lookup"><span data-stu-id="29a31-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a31-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29a31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29a31-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29a31-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="29a31-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29a31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29a31-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29a31-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="29a31-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29a31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29a31-124"><dt>Adoctint. h (incluir Wbemdisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29a31-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="29a31-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="29a31-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="29a31-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29a31-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="29a31-127">DLL</span><span class="sxs-lookup"><span data-stu-id="29a31-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a31-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29a31-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="29a31-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="29a31-129">CLSID</span></span><br/>                    | <span data-ttu-id="29a31-130">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="29a31-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="29a31-131">IID</span><span class="sxs-lookup"><span data-stu-id="29a31-131">IID</span></span><br/>                      | <span data-ttu-id="29a31-132">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="29a31-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




