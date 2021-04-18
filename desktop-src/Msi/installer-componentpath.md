---
description: A propriedade ComponentPath é uma propriedade somente leitura que retorna o caminho completo para um componente instalado. Se o caminho da chave do componente for uma chave do registro, a chave do registro será retornada.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Propriedade Installer. ComponentPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752040"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="22909-104">Propriedade Installer. ComponentPath</span><span class="sxs-lookup"><span data-stu-id="22909-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="22909-105">A propriedade **ComponentPath** é uma propriedade somente leitura que retorna o caminho completo para um componente instalado.</span><span class="sxs-lookup"><span data-stu-id="22909-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="22909-106">Se o caminho da chave do componente for uma chave do registro, a chave do registro será retornada.</span><span class="sxs-lookup"><span data-stu-id="22909-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="22909-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="22909-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="22909-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22909-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="22909-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="22909-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="22909-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="22909-110">Remarks</span></span>

<span data-ttu-id="22909-111">Se o componente for uma chave do registro, as raízes do registro serão representadas numericamente.</span><span class="sxs-lookup"><span data-stu-id="22909-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="22909-112">Por exemplo, um caminho de registro de "HKEY \_ Current \_ user \\ software \\ Microsoft" seria retornado como "01: \\ software \\ Microsoft".</span><span class="sxs-lookup"><span data-stu-id="22909-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="22909-113">As raízes do registro retornadas são definidas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="22909-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="22909-114">Root</span><span class="sxs-lookup"><span data-stu-id="22909-114">Root</span></span>                    | <span data-ttu-id="22909-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="22909-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="22909-116">\_raiz de classes hKey \_</span><span class="sxs-lookup"><span data-stu-id="22909-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="22909-117">00</span><span class="sxs-lookup"><span data-stu-id="22909-117">00</span></span>             |
| <span data-ttu-id="22909-118">HKEY \_ Current \_ User</span><span class="sxs-lookup"><span data-stu-id="22909-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="22909-119">01</span><span class="sxs-lookup"><span data-stu-id="22909-119">01</span></span>             |
| <span data-ttu-id="22909-120">\_máquina local \_ HKEY</span><span class="sxs-lookup"><span data-stu-id="22909-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="22909-121">02</span><span class="sxs-lookup"><span data-stu-id="22909-121">02</span></span>             |
| <span data-ttu-id="22909-122">usuários de HKEY \_</span><span class="sxs-lookup"><span data-stu-id="22909-122">HKEY\_USERS</span></span>             | <span data-ttu-id="22909-123">03</span><span class="sxs-lookup"><span data-stu-id="22909-123">03</span></span>             |
| <span data-ttu-id="22909-124">\_dados de desempenho de hKey \_</span><span class="sxs-lookup"><span data-stu-id="22909-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="22909-125">04</span><span class="sxs-lookup"><span data-stu-id="22909-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="22909-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22909-126">Requirements</span></span>



| <span data-ttu-id="22909-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="22909-127">Requirement</span></span> | <span data-ttu-id="22909-128">Valor</span><span class="sxs-lookup"><span data-stu-id="22909-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22909-129">Versão</span><span class="sxs-lookup"><span data-stu-id="22909-129">Version</span></span><br/> | <span data-ttu-id="22909-130">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="22909-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="22909-131">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="22909-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="22909-132">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="22909-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="22909-133">DLL</span><span class="sxs-lookup"><span data-stu-id="22909-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="22909-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22909-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="22909-135">IID</span><span class="sxs-lookup"><span data-stu-id="22909-135">IID</span></span><br/>     | <span data-ttu-id="22909-136">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="22909-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="22909-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="22909-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22909-138">**MsiGetComponentPath**</span><span class="sxs-lookup"><span data-stu-id="22909-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




