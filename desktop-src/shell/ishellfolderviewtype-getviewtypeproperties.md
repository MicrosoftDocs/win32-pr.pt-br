---
description: Obtém as propriedades da exibição.
title: 'Método IShellFolderViewType:: GetViewTypeProperties'
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
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967494"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="ed684-103">Método IShellFolderViewType:: GetViewTypeProperties</span><span class="sxs-lookup"><span data-stu-id="ed684-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="ed684-104">Obtém as propriedades da exibição.</span><span class="sxs-lookup"><span data-stu-id="ed684-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed684-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed684-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ed684-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed684-107">*PIDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed684-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed684-108">Tipo: **PCUITEMID \_ filho**</span><span class="sxs-lookup"><span data-stu-id="ed684-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="ed684-109">UM PIDL.</span><span class="sxs-lookup"><span data-stu-id="ed684-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="ed684-110">*pdwFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed684-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed684-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="ed684-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="ed684-112">Um ponteiro para uma variável de inteiro sem sinal que recebe as propriedades da exibição, que indicam o que fazer quando a exibição é selecionada.</span><span class="sxs-lookup"><span data-stu-id="ed684-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="ed684-113">Os sinalizadores podem ser qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed684-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="ed684-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ notificar \_ Create*\* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ed684-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG\_NOTIFY\_CREATE*\* (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="ed684-115">Crie um item de exibição se não existir.</span><span class="sxs-lookup"><span data-stu-id="ed684-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="ed684-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFICAr \_ Resort** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ed684-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="ed684-117">Reinsira PIDL e reclassifique.</span><span class="sxs-lookup"><span data-stu-id="ed684-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed684-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed684-118">Return value</span></span>

<span data-ttu-id="ed684-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ed684-119">Type: **HRESULT**</span></span>

<span data-ttu-id="ed684-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ed684-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed684-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed684-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed684-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed684-122">Requirements</span></span>



| <span data-ttu-id="ed684-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed684-123">Requirement</span></span> | <span data-ttu-id="ed684-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ed684-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed684-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed684-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ed684-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed684-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed684-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed684-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ed684-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed684-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ed684-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ed684-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed684-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed684-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




