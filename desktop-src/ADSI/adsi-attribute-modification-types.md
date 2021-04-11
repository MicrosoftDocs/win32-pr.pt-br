---
title: Tipos de modificação de atributo ADSI (IADs. h)
description: Usado com o membro dwControlCode da \_ estrutura de informações attr do ADS \_ para especificar o tipo de operação a ser executada quando um atributo é modificado com o método IDirectoryObject setobjectattributes.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- ADSI tipos de modificação de atributo
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009080"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="2d6d9-104">Tipos de modificação de atributo ADSI</span><span class="sxs-lookup"><span data-stu-id="2d6d9-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="2d6d9-105">As constantes a seguir são usadas com o membro **dwControlCode** da estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para especificar o tipo de operação a ser executada quando um atributo é modificado com o método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="2d6d9-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="2d6d9-106">Para obter mais informações sobre como usar esses valores, consulte [modificando atributos com ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="2d6d9-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="2d6d9-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_atributo attr do ADS \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6d9-108">1</span><span class="sxs-lookup"><span data-stu-id="2d6d9-108">1</span></span>
</dt> <dt>



<span data-ttu-id="2d6d9-109">Faz com que todos os valores de atributo sejam removidos de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d6d9-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_atualização de attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6d9-111">2</span><span class="sxs-lookup"><span data-stu-id="2d6d9-111">2</span></span>
</dt> <dt>



<span data-ttu-id="2d6d9-112">Faz com que os valores de atributo especificados sejam atualizados.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d6d9-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_atributo attr do ADS \_ Append**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6d9-114">3</span><span class="sxs-lookup"><span data-stu-id="2d6d9-114">3</span></span>
</dt> <dt>



<span data-ttu-id="2d6d9-115">Faz com que os valores de atributo especificados sejam acrescentados aos valores de atributo existentes.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d6d9-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**\_exclusão de attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6d9-117">4</span><span class="sxs-lookup"><span data-stu-id="2d6d9-117">4</span></span>
</dt> <dt>



<span data-ttu-id="2d6d9-118">Faz com que os valores de atributo especificados sejam removidos de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d6d9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d6d9-119">Remarks</span></span>

<span data-ttu-id="2d6d9-120">Essas constantes devem ser usadas com a estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) no método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="2d6d9-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="2d6d9-121">Essas constantes não devem ser confundidas com membros da [**enumeração \_ \_ \_ enum da operação de propriedade ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , que devem ser usadas com o método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="2d6d9-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d6d9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d6d9-122">Requirements</span></span>



| <span data-ttu-id="2d6d9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d6d9-123">Requirement</span></span> | <span data-ttu-id="2d6d9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2d6d9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2d6d9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d6d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d6d9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d6d9-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="2d6d9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d6d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d6d9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d6d9-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="2d6d9-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d6d9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d6d9-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d6d9-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d6d9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d6d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d6d9-132">**\_informações de attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="2d6d9-133">**IDirectoryObject:: setobjectattributes**</span><span class="sxs-lookup"><span data-stu-id="2d6d9-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="2d6d9-134">Modificando atributos com ADSI</span><span class="sxs-lookup"><span data-stu-id="2d6d9-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





