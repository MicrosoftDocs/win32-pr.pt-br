---
description: Define o nome amigável do perfil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Método IScanProfile:: SetName (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788662"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="2a474-103">Método IScanProfile:: SetName</span><span class="sxs-lookup"><span data-stu-id="2a474-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="2a474-104">Define o nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="2a474-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a474-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a474-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="2a474-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a474-107">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a474-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a474-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2a474-108">Type: **BSTR**</span></span>

<span data-ttu-id="2a474-109">O nome amigável do perfil.</span><span class="sxs-lookup"><span data-stu-id="2a474-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a474-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a474-110">Return value</span></span>

<span data-ttu-id="2a474-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2a474-111">Type: **HRESULT**</span></span>

<span data-ttu-id="2a474-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2a474-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a474-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a474-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a474-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a474-114">Remarks</span></span>

<span data-ttu-id="2a474-115">Esse método é necessário porque o GUID de um perfil não pode ser usado para exibir o perfil de verificação para um usuário.</span><span class="sxs-lookup"><span data-stu-id="2a474-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="2a474-116">Um usuário pode alterar o nome amigável de um perfil com o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2a474-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="2a474-117">As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="2a474-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="2a474-118">Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.</span><span class="sxs-lookup"><span data-stu-id="2a474-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a474-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a474-119">Requirements</span></span>



| <span data-ttu-id="2a474-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a474-120">Requirement</span></span> | <span data-ttu-id="2a474-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a474-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a474-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a474-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a474-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a474-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2a474-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a474-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a474-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a474-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a474-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a474-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a474-127"><dt>ScanProfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a474-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="2a474-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="2a474-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a474-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a474-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




