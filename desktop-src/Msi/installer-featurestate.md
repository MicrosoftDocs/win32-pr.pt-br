---
description: A propriedade Featurestate somente leitura retorna o estado instalado de um recurso.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Propriedade Installer. Featurestate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747972"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="1fae8-103">Propriedade Installer. Featurestate</span><span class="sxs-lookup"><span data-stu-id="1fae8-103">Installer.FeatureState property</span></span>

<span data-ttu-id="1fae8-104">A propriedade **featurestate** somente leitura retorna o estado instalado de um recurso.</span><span class="sxs-lookup"><span data-stu-id="1fae8-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="1fae8-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1fae8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fae8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fae8-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="1fae8-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1fae8-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1fae8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fae8-108">Remarks</span></span>

<span data-ttu-id="1fae8-109">Essa propriedade retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1fae8-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="1fae8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1fae8-110">Value</span></span>                     | <span data-ttu-id="1fae8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fae8-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="1fae8-112">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="1fae8-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="1fae8-113">O recurso não está instalado.</span><span class="sxs-lookup"><span data-stu-id="1fae8-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="1fae8-114">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="1fae8-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="1fae8-115">O recurso é anunciado.</span><span class="sxs-lookup"><span data-stu-id="1fae8-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="1fae8-116">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="1fae8-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="1fae8-117">O recurso é instalado para ser executado localmente.</span><span class="sxs-lookup"><span data-stu-id="1fae8-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="1fae8-118">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="1fae8-118">msiInstallStateSource</span></span>     | <span data-ttu-id="1fae8-119">O recurso é instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="1fae8-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="1fae8-120">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="1fae8-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="1fae8-121">Um parâmetro inválido foi passado para a função.</span><span class="sxs-lookup"><span data-stu-id="1fae8-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="1fae8-122">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="1fae8-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="1fae8-123">O código do produto ou a ID do recurso é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1fae8-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="1fae8-124">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="1fae8-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="1fae8-125">Os dados de configuração estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="1fae8-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="1fae8-126">A propriedade **featurestate** não valida se o recurso está acessível.</span><span class="sxs-lookup"><span data-stu-id="1fae8-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fae8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fae8-127">Requirements</span></span>



| <span data-ttu-id="1fae8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fae8-128">Requirement</span></span> | <span data-ttu-id="1fae8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1fae8-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fae8-130">Versão</span><span class="sxs-lookup"><span data-stu-id="1fae8-130">Version</span></span><br/> | <span data-ttu-id="1fae8-131">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1fae8-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1fae8-132">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1fae8-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1fae8-133">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fae8-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1fae8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1fae8-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="1fae8-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fae8-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1fae8-136">IID</span><span class="sxs-lookup"><span data-stu-id="1fae8-136">IID</span></span><br/>     | <span data-ttu-id="1fae8-137">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1fae8-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="1fae8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fae8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fae8-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="1fae8-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




