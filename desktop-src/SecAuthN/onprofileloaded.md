---
description: Verifica se o perfil de usuário online está carregado.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Função OnProfileLoaded (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662133"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="958f6-103">Função OnProfileLoaded</span><span class="sxs-lookup"><span data-stu-id="958f6-103">OnProfileLoaded function</span></span>

<span data-ttu-id="958f6-104">Verifica se o perfil de usuário online está carregado.</span><span class="sxs-lookup"><span data-stu-id="958f6-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="958f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="958f6-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="958f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="958f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958f6-107">*ProviderHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="958f6-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958f6-108">O identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="958f6-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="958f6-109">*UserToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="958f6-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958f6-110">Token do usuário cujo perfil está sendo carregado ou descarregado.</span><span class="sxs-lookup"><span data-stu-id="958f6-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="958f6-111">*Carregado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="958f6-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958f6-112">**True** se o perfil tiver sido carregado.</span><span class="sxs-lookup"><span data-stu-id="958f6-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958f6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="958f6-113">Return value</span></span>

<span data-ttu-id="958f6-114">Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="958f6-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="958f6-115">Se a função falhar, a função retornará um código de erro diferente de zero que é um erro específico do provedor para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="958f6-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="958f6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="958f6-116">Remarks</span></span>

<span data-ttu-id="958f6-117">Essa função é chamada cada vez que a função [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) é chamada.</span><span class="sxs-lookup"><span data-stu-id="958f6-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="958f6-118">Ele não está sincronizado com **LoadUserProfile**; ou seja, **LoadUserProfile** pode ter retornado e o perfil pode ter sido descarregado pela hora em que a função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="958f6-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="958f6-119">Essa função pode ser chamada mais de uma vez mesmo quando o perfil tiver sido carregado.</span><span class="sxs-lookup"><span data-stu-id="958f6-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="958f6-120">O provedor de identidade não deve supor que uma chamada para essa função com *Loaded* igual a true será seguida por uma chamada com *Loaded* igual a false.</span><span class="sxs-lookup"><span data-stu-id="958f6-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="958f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="958f6-121">Requirements</span></span>



| <span data-ttu-id="958f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="958f6-122">Requirement</span></span> | <span data-ttu-id="958f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="958f6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="958f6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="958f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="958f6-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="958f6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="958f6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="958f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="958f6-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="958f6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="958f6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="958f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="958f6-129"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="958f6-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
