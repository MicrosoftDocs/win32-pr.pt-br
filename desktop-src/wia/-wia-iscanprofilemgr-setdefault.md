---
description: Define o perfil de verificação especificado como o perfil padrão.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Método IScanProfileMgr:: SetDefault (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811773"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="b3703-103">Método IScanProfileMgr:: SetDefault</span><span class="sxs-lookup"><span data-stu-id="b3703-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="b3703-104">Define o perfil de verificação especificado como o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="b3703-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3703-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3703-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="b3703-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3703-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3703-107">*pScanProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3703-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3703-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b3703-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="b3703-109">Um ponteiro para o perfil.</span><span class="sxs-lookup"><span data-stu-id="b3703-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3703-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3703-110">Return value</span></span>

<span data-ttu-id="b3703-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b3703-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b3703-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b3703-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3703-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3703-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3703-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3703-114">Remarks</span></span>

<span data-ttu-id="b3703-115">Use o método **IScanProfileMgr:: SetDefault** para adicionar um `<Default>` elemento ao perfil ou para remover esse elemento do perfil padrão anterior do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3703-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="b3703-116">Use o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) para alterar o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="b3703-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3703-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3703-117">Requirements</span></span>



| <span data-ttu-id="b3703-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3703-118">Requirement</span></span> | <span data-ttu-id="b3703-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b3703-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3703-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3703-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3703-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3703-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b3703-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3703-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3703-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3703-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3703-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3703-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3703-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3703-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="b3703-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="b3703-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3703-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3703-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3703-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3703-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3703-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="b3703-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="b3703-130">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="b3703-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




