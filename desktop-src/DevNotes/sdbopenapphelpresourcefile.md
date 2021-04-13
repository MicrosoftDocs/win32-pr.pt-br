---
description: Carrega o arquivo de recurso AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Função SdbOpenApphelpResourceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370429"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="f3530-103">Função SdbOpenApphelpResourceFile</span><span class="sxs-lookup"><span data-stu-id="f3530-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="f3530-104">Carrega o arquivo de recurso AppHelp.</span><span class="sxs-lookup"><span data-stu-id="f3530-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3530-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3530-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="f3530-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3530-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3530-107">*pwszACResourceFile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f3530-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3530-108">O caminho para o arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f3530-108">The path to the resource file.</span></span> <span data-ttu-id="f3530-109">Se esse parâmetro for **NULL**, a DLL de recurso local será aberta.</span><span class="sxs-lookup"><span data-stu-id="f3530-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3530-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3530-110">Return value</span></span>

<span data-ttu-id="f3530-111">A função retorna um identificador para o arquivo de recurso aberto.</span><span class="sxs-lookup"><span data-stu-id="f3530-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3530-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3530-112">Requirements</span></span>



| <span data-ttu-id="f3530-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3530-113">Requirement</span></span> | <span data-ttu-id="f3530-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f3530-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3530-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3530-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3530-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3530-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3530-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3530-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3530-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3530-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f3530-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f3530-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3530-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3530-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




