---
description: Recupera o diretório AppPatch do sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Função SdbGetAppPatchDir
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088816"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="5ed66-103">Função SdbGetAppPatchDir</span><span class="sxs-lookup"><span data-stu-id="5ed66-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="5ed66-104">Recupera o diretório AppPatch do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ed66-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ed66-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="5ed66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ed66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed66-107">*hSDB* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5ed66-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed66-108">Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed66-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5ed66-109">*szAppPatchPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ed66-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed66-110">O caminho resultante.</span><span class="sxs-lookup"><span data-stu-id="5ed66-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="5ed66-111">*cchSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed66-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed66-112">O tamanho do buffer *szAppPatchPath* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ed66-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="5ed66-113">Se a função falhar, esse parâmetro será definido como a cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="5ed66-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed66-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ed66-114">Return value</span></span>

<span data-ttu-id="5ed66-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5ed66-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed66-116">Requirements</span></span>



| <span data-ttu-id="5ed66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed66-117">Requirement</span></span> | <span data-ttu-id="5ed66-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed66-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed66-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed66-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ed66-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ed66-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed66-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ed66-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5ed66-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed66-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed66-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed66-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed66-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ed66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed66-126">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="5ed66-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




