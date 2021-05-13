---
description: Obtém as propriedades da exibição.
title: Método IShellFolderViewType::GetViewTypeProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842697"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="8d52a-103">Método IShellFolderViewType::GetViewTypeProperties</span><span class="sxs-lookup"><span data-stu-id="8d52a-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="8d52a-104">Obtém as propriedades da exibição.</span><span class="sxs-lookup"><span data-stu-id="8d52a-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d52a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d52a-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8d52a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d52a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d52a-107">*pidl* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="8d52a-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d52a-108">Tipo: **PCUITEMID \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="8d52a-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="8d52a-109">Um PIDL.</span><span class="sxs-lookup"><span data-stu-id="8d52a-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="8d52a-110">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8d52a-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d52a-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="8d52a-111">Type: **DWORD\***</span></span>

<span data-ttu-id="8d52a-112">Um ponteiro para uma variável de inteiro sem sinal que recebe as propriedades de exibição, que indicam o que fazer quando a exibição é selecionada.</span><span class="sxs-lookup"><span data-stu-id="8d52a-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="8d52a-113">Os sinalizadores podem ser qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d52a-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="8d52a-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8d52a-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="8d52a-115">Crie o item de exibição se não estiver lá.</span><span class="sxs-lookup"><span data-stu-id="8d52a-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="8d52a-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8d52a-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="8d52a-117">Reinserir o PIDL e classificar novamente.</span><span class="sxs-lookup"><span data-stu-id="8d52a-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d52a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d52a-118">Return value</span></span>

<span data-ttu-id="8d52a-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d52a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8d52a-120">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="8d52a-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d52a-121">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8d52a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d52a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d52a-122">Requirements</span></span>



| <span data-ttu-id="8d52a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d52a-123">Requirement</span></span> | <span data-ttu-id="8d52a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8d52a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d52a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d52a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8d52a-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d52a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d52a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d52a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8d52a-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d52a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d52a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8d52a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d52a-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d52a-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




