---
description: A propriedade MSIRMSHUTDOWN determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propriedade MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780948"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="bf5fe-103">Propriedade MSIRMSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="bf5fe-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="bf5fe-104">A propriedade **MSIRMSHUTDOWN** determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="bf5fe-105">Valor</span><span class="sxs-lookup"><span data-stu-id="bf5fe-105">Value</span></span>



| <span data-ttu-id="bf5fe-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bf5fe-106">Value</span></span>                                                                        | <span data-ttu-id="bf5fe-107">Significado</span><span class="sxs-lookup"><span data-stu-id="bf5fe-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf5fe-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fe-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="bf5fe-109">Os processos ou serviços que estão usando arquivos afetados pela atualização estão desligados.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="bf5fe-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fe-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="bf5fe-111">Os processos ou serviços que estão usando arquivos afetados pela atualização e que não respondem ao [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md)são forçados a desligar.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="bf5fe-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fe-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="bf5fe-113">Os processos ou serviços que estão usando arquivos afetados pela atualização serão desligados somente se tiverem sido registrados para uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="bf5fe-114">Se algum processo ou serviço não tiver sido registrado para uma reinicialização, não haverá processos ou serviços desligados.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf5fe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf5fe-115">Remarks</span></span>

<span data-ttu-id="bf5fe-116">A propriedade **MSIRMSHUTDOWN** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf5fe-117">Requirements</span></span>



| <span data-ttu-id="bf5fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf5fe-118">Requirement</span></span> | <span data-ttu-id="bf5fe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bf5fe-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5fe-120">Versão</span><span class="sxs-lookup"><span data-stu-id="bf5fe-120">Version</span></span><br/> | <span data-ttu-id="bf5fe-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bf5fe-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bf5fe-123">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bf5fe-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf5fe-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf5fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5fe-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf5fe-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bf5fe-126">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="bf5fe-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
