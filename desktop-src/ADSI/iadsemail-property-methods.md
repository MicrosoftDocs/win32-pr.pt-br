---
title: Métodos de propriedade IADsEmail (IADs. h)
description: O método Property da interface IADsEmail define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsEmail
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369821"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="f4f99-105">Métodos de propriedade IADsEmail</span><span class="sxs-lookup"><span data-stu-id="f4f99-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="f4f99-106">O método Property da interface [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4f99-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="f4f99-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f4f99-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f4f99-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f4f99-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f4f99-109">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="f4f99-109">**Address**</span></span>
<span data-ttu-id="f4f99-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f4f99-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f4f99-111">O endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="f4f99-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="f4f99-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f4f99-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f4f99-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f4f99-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4f99-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4f99-114">**Type**</span></span>
<span data-ttu-id="f4f99-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f4f99-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f4f99-116">O tipo da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f4f99-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="f4f99-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f4f99-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f4f99-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="f4f99-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="f4f99-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f99-119">Requirements</span></span>



| <span data-ttu-id="f4f99-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f99-120">Requirement</span></span> | <span data-ttu-id="f4f99-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f99-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f99-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4f99-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f99-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4f99-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4f99-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4f99-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f99-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4f99-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4f99-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4f99-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4f99-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f99-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f4f99-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f4f99-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4f99-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f99-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4f99-130">IID</span><span class="sxs-lookup"><span data-stu-id="f4f99-130">IID</span></span><br/>                      | <span data-ttu-id="f4f99-131">IID \_ IADsEmail é definido como 97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="f4f99-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f4f99-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4f99-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f99-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="f4f99-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="f4f99-134">**EMAIL do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="f4f99-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





