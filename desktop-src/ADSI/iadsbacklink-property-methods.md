---
title: Métodos de propriedade IADsBackLink (IADs. h)
description: O método Property da interface IADsBackLink define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsBackLink
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086048"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="5b4c2-105">Métodos de propriedade IADsBackLink</span><span class="sxs-lookup"><span data-stu-id="5b4c2-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="5b4c2-106">O método Property da interface [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="5b4c2-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5b4c2-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5b4c2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b4c2-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5b4c2-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-109">**ObjectName**</span></span>
<span data-ttu-id="5b4c2-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5b4c2-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5b4c2-111">O nome de um objeto ao qual o atributo de **back link** está anexado.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="5b4c2-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b4c2-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5b4c2-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b4c2-114">**Remotoid**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-114">**RemoteID**</span></span>
<span data-ttu-id="5b4c2-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5b4c2-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5b4c2-116">O identificador do servidor remoto que requer uma referência externa do objeto especificado por **objectname**.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="5b4c2-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b4c2-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5b4c2-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="5b4c2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4c2-119">Requirements</span></span>



| <span data-ttu-id="5b4c2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4c2-120">Requirement</span></span> | <span data-ttu-id="5b4c2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5b4c2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4c2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b4c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4c2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b4c2-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b4c2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b4c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4c2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b4c2-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b4c2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b4c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4c2-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b4c2-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5b4c2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5b4c2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b4c2-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b4c2-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b4c2-130">IID</span><span class="sxs-lookup"><span data-stu-id="5b4c2-130">IID</span></span><br/>                      | <span data-ttu-id="5b4c2-131">IID \_ IADsBackLink é definido como FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="5b4c2-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5b4c2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b4c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b4c2-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="5b4c2-134">**\_BACKLINK ADS**</span><span class="sxs-lookup"><span data-stu-id="5b4c2-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





