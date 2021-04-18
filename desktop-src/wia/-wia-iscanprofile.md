---
description: A interface IScanProfile representa um único perfil de verificação e permite que os aplicativos definam e obtenham as propriedades do perfil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interface IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764404"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="82aec-103">Interface IScanProfile</span><span class="sxs-lookup"><span data-stu-id="82aec-103">IScanProfile interface</span></span>

<span data-ttu-id="82aec-104">A interface **IScanProfile** representa um único perfil de verificação e permite que os aplicativos definam e obtenham as propriedades do perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="82aec-105">Membros</span><span class="sxs-lookup"><span data-stu-id="82aec-105">Members</span></span>

<span data-ttu-id="82aec-106">A interface **IScanProfile** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="82aec-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="82aec-107">**IScanProfile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82aec-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="82aec-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="82aec-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82aec-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="82aec-109">Methods</span></span>

<span data-ttu-id="82aec-110">A interface **IScanProfile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="82aec-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="82aec-111">Método</span><span class="sxs-lookup"><span data-stu-id="82aec-111">Method</span></span>                                                     | <span data-ttu-id="82aec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="82aec-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82aec-113">**GetAllPropIDs**</span><span class="sxs-lookup"><span data-stu-id="82aec-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="82aec-114">Obtém todas as IDs de propriedade disponíveis em um perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="82aec-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="82aec-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="82aec-116">Retorna a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82aec-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="82aec-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="82aec-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="82aec-118">Retorna o GUID do perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="82aec-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="82aec-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="82aec-120">Obtém o GUID da categoria do item WIA 2,0 ao qual o perfil está associado.</span><span class="sxs-lookup"><span data-stu-id="82aec-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="82aec-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="82aec-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="82aec-122">Obtém o nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="82aec-123">**GetNumPropIDS**</span><span class="sxs-lookup"><span data-stu-id="82aec-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="82aec-124">Obtém o número de IDs de propriedade em um perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="82aec-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="82aec-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="82aec-126">Obtém o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="82aec-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="82aec-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="82aec-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="82aec-128">Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associado.</span><span class="sxs-lookup"><span data-stu-id="82aec-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="82aec-129">**Removerproperty**</span><span class="sxs-lookup"><span data-stu-id="82aec-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="82aec-130">Remove uma lista especificada de propriedades filho no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="82aec-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="82aec-131">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="82aec-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="82aec-132">Salva as alterações em um perfil no disco.</span><span class="sxs-lookup"><span data-stu-id="82aec-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="82aec-133">**SetItem**</span><span class="sxs-lookup"><span data-stu-id="82aec-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="82aec-134">Define o GUID da categoria do item WIA 2,0 ao qual o perfil está associado.</span><span class="sxs-lookup"><span data-stu-id="82aec-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="82aec-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="82aec-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="82aec-136">Define o nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="82aec-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="82aec-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="82aec-138">Define o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="82aec-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="82aec-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="82aec-139">Remarks</span></span>

<span data-ttu-id="82aec-140">Qualquer dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) pode ter um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="82aec-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="82aec-141">No entanto, **IWiaItem2** itens dos \_ tipos \_ grupo WIA concluído \_ arquivo e \_ raiz da categoria WIA \_ não podem ter perfis.</span><span class="sxs-lookup"><span data-stu-id="82aec-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="82aec-142">Se um perfil de verificação for salvo usando o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , ele será armazenado como um arquivo XML em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="82aec-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="82aec-143">Para criar uma instância de um objeto **IScanProfile** , use o método [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="82aec-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="82aec-144">Para obter uma referência a um perfil de verificação que já foi salvo no disco, use o método [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="82aec-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="82aec-145">Todos os perfis de verificação têm os seguintes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="82aec-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="82aec-146">O perfil padrão de um dispositivo também tem um `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="82aec-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="82aec-147">Os `<ProfileGUID>` `<DeviceID>` elementos e não podem ser alterados depois que o perfil é criado.</span><span class="sxs-lookup"><span data-stu-id="82aec-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="82aec-148">Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser alterados depois que o perfil é criado.</span><span class="sxs-lookup"><span data-stu-id="82aec-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="82aec-149">O `<Default>` elemento pode ser adicionado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="82aec-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="82aec-150">Isso pode ser feito de forma programática com os métodos [**IScanProfile:: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="82aec-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="82aec-151">Essas propriedades também podem ser alteradas pelos usuários por meio do método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="82aec-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="82aec-152">O `<Properties>` elemento contém `<Property>` filhos.</span><span class="sxs-lookup"><span data-stu-id="82aec-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="82aec-153">Use-os para adicionar qualquer propriedade de dispositivo ou item WIA 2,0 ao perfil.</span><span class="sxs-lookup"><span data-stu-id="82aec-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="82aec-154">Você também pode desenvolver sua própria imagem aquisição `<Property>` filhos.</span><span class="sxs-lookup"><span data-stu-id="82aec-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="82aec-155">Isso torna o esquema do perfil de verificação extensível.</span><span class="sxs-lookup"><span data-stu-id="82aec-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="82aec-156">(Para obter mais informações sobre como estender o esquema, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="82aec-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="82aec-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82aec-157">Requirements</span></span>



| <span data-ttu-id="82aec-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="82aec-158">Requirement</span></span> | <span data-ttu-id="82aec-159">Valor</span><span class="sxs-lookup"><span data-stu-id="82aec-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="82aec-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82aec-160">Minimum supported client</span></span><br/> | <span data-ttu-id="82aec-161">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82aec-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="82aec-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82aec-162">Minimum supported server</span></span><br/> | <span data-ttu-id="82aec-163">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82aec-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82aec-164">INSERI</span><span class="sxs-lookup"><span data-stu-id="82aec-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82aec-165"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82aec-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82aec-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="82aec-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82aec-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="82aec-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="82aec-168">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="82aec-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
