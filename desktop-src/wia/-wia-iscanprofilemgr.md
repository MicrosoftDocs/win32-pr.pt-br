---
description: A interface IScanProfileMgr fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interface IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757055"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="81df5-103">Interface IScanProfileMgr</span><span class="sxs-lookup"><span data-stu-id="81df5-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="81df5-104">A interface **IScanProfileMgr** fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação.</span><span class="sxs-lookup"><span data-stu-id="81df5-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="81df5-105">Membros</span><span class="sxs-lookup"><span data-stu-id="81df5-105">Members</span></span>

<span data-ttu-id="81df5-106">A interface **IScanProfileMgr** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="81df5-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="81df5-107">**IScanProfileMgr** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81df5-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="81df5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="81df5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81df5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="81df5-109">Methods</span></span>

<span data-ttu-id="81df5-110">A interface **IScanProfileMgr** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="81df5-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="81df5-111">Método</span><span class="sxs-lookup"><span data-stu-id="81df5-111">Method</span></span>                                                                              | <span data-ttu-id="81df5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="81df5-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81df5-113">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="81df5-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="81df5-114">Cria um perfil de verificação vazio e o associa a um scanner ou a outro item WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="81df5-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="81df5-115">**DeleteAllProfiles**</span><span class="sxs-lookup"><span data-stu-id="81df5-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="81df5-116">Exclui todos os perfis de verificação associados ao dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="81df5-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="81df5-117">**DeleteAllProfilesForUser**</span><span class="sxs-lookup"><span data-stu-id="81df5-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="81df5-118">Exclui todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="81df5-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="81df5-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="81df5-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="81df5-120">Exclui o perfil de exame especificado.</span><span class="sxs-lookup"><span data-stu-id="81df5-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="81df5-121">**GetDefaultProfile**</span><span class="sxs-lookup"><span data-stu-id="81df5-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="81df5-122">Obtém o perfil de exame padrão.</span><span class="sxs-lookup"><span data-stu-id="81df5-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="81df5-123">**GetNumProfiles**</span><span class="sxs-lookup"><span data-stu-id="81df5-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="81df5-124">Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="81df5-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="81df5-125">**GetNumProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="81df5-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="81df5-126">Obtém o número de perfis de verificação para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81df5-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="81df5-127">**Getperfis**</span><span class="sxs-lookup"><span data-stu-id="81df5-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="81df5-128">Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="81df5-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="81df5-129">**GetProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="81df5-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="81df5-130">Obtém todos os perfis de verificação associados a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81df5-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="81df5-131">**OpenProfile**</span><span class="sxs-lookup"><span data-stu-id="81df5-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="81df5-132">Abre um perfil de verificação que foi salvo no disco como um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="81df5-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="81df5-133">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="81df5-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="81df5-134">Enumera novamente todos os perfis de verificação no sistema.</span><span class="sxs-lookup"><span data-stu-id="81df5-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="81df5-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="81df5-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="81df5-136">Define o perfil de verificação especificado como o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="81df5-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="81df5-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="81df5-137">Remarks</span></span>

<span data-ttu-id="81df5-138">Para criar um objeto **IScanProfileMgr** , use o método [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="81df5-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="81df5-139">Se um perfil de verificação for salvo usando o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , ele será armazenado como um arquivo XML em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="81df5-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="81df5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81df5-140">Requirements</span></span>



| <span data-ttu-id="81df5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="81df5-141">Requirement</span></span> | <span data-ttu-id="81df5-142">Valor</span><span class="sxs-lookup"><span data-stu-id="81df5-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="81df5-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81df5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="81df5-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81df5-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="81df5-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81df5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="81df5-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81df5-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81df5-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81df5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="81df5-148"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="81df5-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="81df5-149">INSERI</span><span class="sxs-lookup"><span data-stu-id="81df5-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81df5-150"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81df5-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81df5-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="81df5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81df5-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="81df5-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="81df5-153">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="81df5-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
