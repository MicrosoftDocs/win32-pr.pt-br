---
title: TfGuidAtom (msctf. h)
description: O tipo de dados TfGuidAtom identifica um GUID no TSF. Um TfGuidAtom é obtido chamando ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085137"
---
# <a name="tfguidatom"></a><span data-ttu-id="46757-105">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="46757-105">TfGuidAtom</span></span>

<span data-ttu-id="46757-106">O tipo de dados **TfGuidAtom** identifica um **GUID** no TSF.</span><span class="sxs-lookup"><span data-stu-id="46757-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="46757-107">Um **TfGuidAtom** é obtido chamando [**ITfCategoryMgr:: RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="46757-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="46757-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="46757-108">Remarks</span></span>

<span data-ttu-id="46757-109">Um valor de **TfGuidAtom** só é válido no processo em que **ITfCategoryMgr:: RegisterGUID** é chamado de.</span><span class="sxs-lookup"><span data-stu-id="46757-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="46757-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46757-110">Requirements</span></span>



| <span data-ttu-id="46757-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="46757-111">Requirement</span></span> | <span data-ttu-id="46757-112">Valor</span><span class="sxs-lookup"><span data-stu-id="46757-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46757-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46757-113">Minimum supported client</span></span><br/> | <span data-ttu-id="46757-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46757-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="46757-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46757-115">Minimum supported server</span></span><br/> | <span data-ttu-id="46757-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46757-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46757-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="46757-117">Redistributable</span></span><br/>          | <span data-ttu-id="46757-118">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46757-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="46757-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46757-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="46757-120"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="46757-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="46757-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="46757-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46757-122"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46757-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46757-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="46757-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46757-124">**ITfCategoryMgr:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="46757-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="46757-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span><span class="sxs-lookup"><span data-stu-id="46757-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="46757-126">**ITfCategoryMgr::RegisterGUID**</span><span class="sxs-lookup"><span data-stu-id="46757-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





