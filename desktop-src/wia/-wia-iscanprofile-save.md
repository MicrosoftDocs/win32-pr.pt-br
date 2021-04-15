---
description: Salva as alterações em um perfil no disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Método IScanProfile:: Save (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502000"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="71246-103">Método IScanProfile:: Save</span><span class="sxs-lookup"><span data-stu-id="71246-103">IScanProfile::Save method</span></span>

<span data-ttu-id="71246-104">Salva as alterações em um perfil no disco.</span><span class="sxs-lookup"><span data-stu-id="71246-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="71246-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71246-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="71246-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71246-106">Parameters</span></span>

<span data-ttu-id="71246-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="71246-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71246-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71246-108">Return value</span></span>

<span data-ttu-id="71246-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71246-109">Type: **HRESULT**</span></span>

<span data-ttu-id="71246-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71246-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71246-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71246-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71246-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="71246-112">Remarks</span></span>

<span data-ttu-id="71246-113">Um perfil de verificação salvo é um arquivo XML armazenado em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="71246-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="71246-114">Se mais de um processo gravar no objeto [**IScanProfile**](-wia-iscanprofile.md) , aquele que chama **IScanProfile:: Save** Last será o único processo cujas alterações são salvas.</span><span class="sxs-lookup"><span data-stu-id="71246-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="71246-115">O método **IScanProfile:: Save** valida o perfil antes de salvar.</span><span class="sxs-lookup"><span data-stu-id="71246-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="71246-116">O perfil é sempre considerado válido, a menos que a categoria do item de aquisição de imagem do Windows (WIA) 2,0 associado ao perfil seja o \_ \_ feed de categoria WIA ou o \_ alimentador de categoria WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="71246-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="71246-117">Se a categoria for o \_ feed de categoria WIA \_ ou o \_ \_ alimentador de categoria WIA, as propriedades a seguir deverão ser válidas para o item, se as propriedades estiverem contidas no perfil:</span><span class="sxs-lookup"><span data-stu-id="71246-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="71246-118">\_brilho de IPS WIA \_</span><span class="sxs-lookup"><span data-stu-id="71246-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="71246-119">\_contraste de IPS WIA \_</span><span class="sxs-lookup"><span data-stu-id="71246-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="71246-120">\_tipo de \_ dados IPA WIA</span><span class="sxs-lookup"><span data-stu-id="71246-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="71246-121">\_XRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="71246-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="71246-122">\_formato IPA \_ WIA</span><span class="sxs-lookup"><span data-stu-id="71246-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="71246-123">Além disso, se a categoria for o \_ alimentador de categorias WIA \_ , \_ a \_ Propriedade tamanho da página IPS WIA \_ deverá ser válida, se estiver presente no perfil.</span><span class="sxs-lookup"><span data-stu-id="71246-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="71246-124">Para obter mais informações sobre essas propriedades, consulte [**constantes de Propriedade do item WIA do scanner**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="71246-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71246-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71246-125">Requirements</span></span>



| <span data-ttu-id="71246-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="71246-126">Requirement</span></span> | <span data-ttu-id="71246-127">Valor</span><span class="sxs-lookup"><span data-stu-id="71246-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="71246-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71246-128">Minimum supported client</span></span><br/> | <span data-ttu-id="71246-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71246-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="71246-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71246-130">Minimum supported server</span></span><br/> | <span data-ttu-id="71246-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71246-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71246-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71246-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="71246-133"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="71246-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="71246-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="71246-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71246-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71246-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71246-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="71246-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71246-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="71246-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="71246-138">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="71246-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




