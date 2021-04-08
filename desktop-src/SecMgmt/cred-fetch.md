---
description: Define valores que determinam como buscar a credencial de uma conta de serviço gerenciado de grupo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumeração de CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922239"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="66210-103">Enumeração de busca de credenciais \_</span><span class="sxs-lookup"><span data-stu-id="66210-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="66210-104">Define valores que determinam como buscar a credencial de uma conta de serviço gerenciado de grupo (gMSA).</span><span class="sxs-lookup"><span data-stu-id="66210-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="66210-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66210-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="66210-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="66210-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66210-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span><span class="sxs-lookup"><span data-stu-id="66210-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="66210-108">Significa que o sistema operacional deve primeiro tentar recuperar a senha do cache local.</span><span class="sxs-lookup"><span data-stu-id="66210-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="66210-109">Se for o momento de buscar a senha, o sistema operacional deverá contatar um controlador de domínio para a senha.</span><span class="sxs-lookup"><span data-stu-id="66210-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="66210-110">Se isso falhar, retorne todas as senhas em cache com o valor de status êxito.</span><span class="sxs-lookup"><span data-stu-id="66210-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="66210-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span><span class="sxs-lookup"><span data-stu-id="66210-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="66210-112">Retorna a credencial DPAPI local para o chamador.</span><span class="sxs-lookup"><span data-stu-id="66210-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="66210-113">Os SSPs ( [*provedores de suporte de segurança*](/windows/desktop/SecGloss/s-gly) ) geralmente não exigem o uso dessa enumeração.</span><span class="sxs-lookup"><span data-stu-id="66210-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="66210-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span><span class="sxs-lookup"><span data-stu-id="66210-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="66210-115">Força o sistema operacional a tentar ler a senha do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="66210-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="66210-116">Durante a hora de substituição da senha, a senha pode ter sido alterada no controlador de domínio e em outros hosts membros, mas o host membro do gMSA reconhece a senha como ainda válida.</span><span class="sxs-lookup"><span data-stu-id="66210-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="66210-117">Isso pode acontecer devido a problemas de distorção de relógio entre diferentes controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="66210-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="66210-118">Quando esse valor é especificado, o sistema operacional determina se pode haver uma possível alteração de senha devido à distorção do relógio e, nesse caso, recupera a senha.</span><span class="sxs-lookup"><span data-stu-id="66210-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="66210-119">Caso contrário, a credencial armazenada em cache será retornada.</span><span class="sxs-lookup"><span data-stu-id="66210-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="66210-120">Se não houver nenhuma credencial armazenada em cache, o sistema operacional tentará obter uma do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="66210-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66210-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66210-121">Requirements</span></span>



| <span data-ttu-id="66210-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66210-122">Requirement</span></span> | <span data-ttu-id="66210-123">Valor</span><span class="sxs-lookup"><span data-stu-id="66210-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66210-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66210-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66210-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="66210-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="66210-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66210-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66210-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="66210-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66210-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66210-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="66210-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="66210-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

