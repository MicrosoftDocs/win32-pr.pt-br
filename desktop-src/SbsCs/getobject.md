---
description: O método GetObject Obtém uma instância de um objeto Microsoft. Windows. ActCtx existente.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Método ActCtx. GetObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647015"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="39582-103">Método ActCtx. GetObject</span><span class="sxs-lookup"><span data-stu-id="39582-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="39582-104">O método **GetObject** Obtém uma instância de um objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existente.</span><span class="sxs-lookup"><span data-stu-id="39582-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39582-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39582-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="39582-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39582-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="39582-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="39582-108">Cadeia de caracteres necessária que indica o objeto.</span><span class="sxs-lookup"><span data-stu-id="39582-108">Required string that indicates the object.</span></span> <span data-ttu-id="39582-109">O nome deve estar no registro em **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.</span><span class="sxs-lookup"><span data-stu-id="39582-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39582-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39582-110">Return value</span></span>

<span data-ttu-id="39582-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="39582-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39582-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39582-112">Requirements</span></span>



| <span data-ttu-id="39582-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="39582-113">Requirement</span></span> | <span data-ttu-id="39582-114">Valor</span><span class="sxs-lookup"><span data-stu-id="39582-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39582-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39582-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39582-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39582-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="39582-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39582-117">Minimum supported server</span></span><br/> | <span data-ttu-id="39582-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39582-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="39582-119">DLL</span><span class="sxs-lookup"><span data-stu-id="39582-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39582-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39582-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="39582-121">IID</span><span class="sxs-lookup"><span data-stu-id="39582-121">IID</span></span><br/>                      | <span data-ttu-id="39582-122">IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="39582-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="39582-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="39582-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39582-124">**Método CreateObject**</span><span class="sxs-lookup"><span data-stu-id="39582-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




