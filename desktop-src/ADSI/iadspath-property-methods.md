---
title: Métodos de propriedade IADsPath (IADs. h)
description: O método Property da interface IADsPath define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPath
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644945"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="add66-105">Métodos de propriedade IADsPath</span><span class="sxs-lookup"><span data-stu-id="add66-105">IADsPath Property Methods</span></span>

<span data-ttu-id="add66-106">O método Property da interface [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="add66-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="add66-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="add66-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="add66-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="add66-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="add66-109">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="add66-109">**Path**</span></span>
<span data-ttu-id="add66-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="add66-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="add66-111">Caminho de um diretório do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="add66-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="add66-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="add66-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="add66-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="add66-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="add66-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="add66-114">**Type**</span></span>
<span data-ttu-id="add66-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="add66-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="add66-116">Tipo de arquivo do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="add66-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="add66-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="add66-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="add66-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="add66-118">Scripting data type: **LONG**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="add66-119">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="add66-119">**VolumeName**</span></span>
<span data-ttu-id="add66-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="add66-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="add66-121">Nome de um volume existente do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="add66-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="add66-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="add66-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="add66-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="add66-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="add66-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add66-124">Requirements</span></span>



| <span data-ttu-id="add66-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="add66-125">Requirement</span></span> | <span data-ttu-id="add66-126">Valor</span><span class="sxs-lookup"><span data-stu-id="add66-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="add66-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="add66-127">Minimum supported client</span></span><br/> | <span data-ttu-id="add66-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="add66-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="add66-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="add66-129">Minimum supported server</span></span><br/> | <span data-ttu-id="add66-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="add66-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="add66-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="add66-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="add66-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="add66-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="add66-133">DLL</span><span class="sxs-lookup"><span data-stu-id="add66-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="add66-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add66-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="add66-135">IID</span><span class="sxs-lookup"><span data-stu-id="add66-135">IID</span></span><br/>                      | <span data-ttu-id="add66-136">IID \_ IADsPath é definido como B287FCD5-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="add66-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="add66-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="add66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add66-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="add66-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="add66-139">**\_caminho ADs**</span><span class="sxs-lookup"><span data-stu-id="add66-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





