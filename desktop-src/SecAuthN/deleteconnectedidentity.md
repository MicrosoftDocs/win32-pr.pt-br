---
description: Exclui a credencial do usuário usada para a identidade conectada.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Função DeleteConnectedIdentity (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010370"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="20fcc-103">Função DeleteConnectedIdentity</span><span class="sxs-lookup"><span data-stu-id="20fcc-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="20fcc-104">Exclui a credencial do usuário usada para a identidade conectada.</span><span class="sxs-lookup"><span data-stu-id="20fcc-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20fcc-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="20fcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20fcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fcc-107">*ProviderHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fcc-108">Identificador do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="20fcc-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="20fcc-109">*UserToken* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20fcc-110">Token do usuário conectado cuja conta será convertida em uma conta local.</span><span class="sxs-lookup"><span data-stu-id="20fcc-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="20fcc-111">Se *UserToken* não for **NULL**, o provedor de identidade usará esse token para carregar o perfil do usuário e limpar os Estados conectados.</span><span class="sxs-lookup"><span data-stu-id="20fcc-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="20fcc-112">Se *UserToken* for **NULL**, o LSA está forçando a desconexão.</span><span class="sxs-lookup"><span data-stu-id="20fcc-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="20fcc-113">O provedor de identidade deve limpar todos os Estados conectados globais nesse usuário, mas o provedor não precisa limpar os Estados conectados no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="20fcc-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="20fcc-114">*Userid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fcc-115">O SID principal do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="20fcc-115">The primary SID of the connected user.</span></span> <span data-ttu-id="20fcc-116">Se *UserToken* não for **NULL**, esse parâmetro será o Sid de usuário do token.</span><span class="sxs-lookup"><span data-stu-id="20fcc-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="20fcc-117">Se *UserToken* for **NULL**, esse parâmetro será usado para identificar o usuário conectado e limpar os Estados de conexão global desse usuário.</span><span class="sxs-lookup"><span data-stu-id="20fcc-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="20fcc-118">*IdentityUserName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fcc-119">O nome de usuário da identidade.</span><span class="sxs-lookup"><span data-stu-id="20fcc-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fcc-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20fcc-120">Return value</span></span>

<span data-ttu-id="20fcc-121">Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20fcc-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="20fcc-122">Se a função falhar, a função poderá retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="20fcc-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="20fcc-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="20fcc-123">Return value</span></span>                                                                                               | <span data-ttu-id="20fcc-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="20fcc-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20fcc-125"><dt>parâmetro de STATUS \_ inválido \_</dt></span><span class="sxs-lookup"><span data-stu-id="20fcc-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="20fcc-126">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="20fcc-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="20fcc-127"><dt>STATUS \_ não é \_ esse \_ usuário</dt></span><span class="sxs-lookup"><span data-stu-id="20fcc-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="20fcc-128">O usuário identificado por *userid* não existe, não está conectado no momento ou não há nenhuma identidade cujo nome de usuário corresponda a *IdentityUserName*.</span><span class="sxs-lookup"><span data-stu-id="20fcc-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="20fcc-129"><dt>STATUS de \_ recursos insuficientes \_</dt></span><span class="sxs-lookup"><span data-stu-id="20fcc-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="20fcc-130">Não há memória suficiente para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="20fcc-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="20fcc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fcc-131">Requirements</span></span>



| <span data-ttu-id="20fcc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fcc-132">Requirement</span></span> | <span data-ttu-id="20fcc-133">Valor</span><span class="sxs-lookup"><span data-stu-id="20fcc-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fcc-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fcc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="20fcc-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="20fcc-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fcc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="20fcc-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="20fcc-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20fcc-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20fcc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="20fcc-139"><dt>Indentitystore. h</dt></span><span class="sxs-lookup"><span data-stu-id="20fcc-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




