---
description: Define o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Método IScanProfile:: SetItem (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761547"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="67ec3-103">Método IScanProfile:: SetItem</span><span class="sxs-lookup"><span data-stu-id="67ec3-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="67ec3-104">Define o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.</span><span class="sxs-lookup"><span data-stu-id="67ec3-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ec3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ec3-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="67ec3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ec3-107">*guidCategory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67ec3-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ec3-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="67ec3-108">Type: **GUID**</span></span>

<span data-ttu-id="67ec3-109">O GUID da categoria do item WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="67ec3-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="67ec3-110">Deve ser uma das \_ constantes da categoria de item IPA do WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67ec3-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ec3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67ec3-111">Return value</span></span>

<span data-ttu-id="67ec3-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="67ec3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="67ec3-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67ec3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67ec3-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67ec3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ec3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ec3-115">Remarks</span></span>

<span data-ttu-id="67ec3-116">Os usuários podem alterar a categoria com o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="67ec3-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="67ec3-117">As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="67ec3-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="67ec3-118">Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.</span><span class="sxs-lookup"><span data-stu-id="67ec3-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ec3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ec3-119">Requirements</span></span>



| <span data-ttu-id="67ec3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ec3-120">Requirement</span></span> | <span data-ttu-id="67ec3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="67ec3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ec3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ec3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67ec3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67ec3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="67ec3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ec3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67ec3-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67ec3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67ec3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67ec3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ec3-127"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="67ec3-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="67ec3-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="67ec3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67ec3-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67ec3-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ec3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="67ec3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ec3-131">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="67ec3-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="67ec3-132">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="67ec3-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




