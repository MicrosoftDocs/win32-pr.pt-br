---
description: A propriedade MSIDISABLERMRESTART determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados e reiniciados para habilitar a instalação da atualização.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propriedade MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752247"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="4c240-103">Propriedade MSIDISABLERMRESTART</span><span class="sxs-lookup"><span data-stu-id="4c240-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="4c240-104">A propriedade **MSIDISABLERMRESTART** determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados e reiniciados para habilitar a instalação da atualização.</span><span class="sxs-lookup"><span data-stu-id="4c240-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="4c240-105">Valor</span><span class="sxs-lookup"><span data-stu-id="4c240-105">Value</span></span>



| <span data-ttu-id="4c240-106">Valor</span><span class="sxs-lookup"><span data-stu-id="4c240-106">Value</span></span>                                                                        | <span data-ttu-id="4c240-107">Significado</span><span class="sxs-lookup"><span data-stu-id="4c240-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c240-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c240-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4c240-109">Todos os serviços do sistema que foram desligados para instalar a atualização são reiniciados.</span><span class="sxs-lookup"><span data-stu-id="4c240-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="4c240-110">Todos os aplicativos que se registraram com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) são reiniciados.</span><span class="sxs-lookup"><span data-stu-id="4c240-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="4c240-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c240-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4c240-112">Os processos que foram desligados usando o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) durante a instalação da atualização não serão reiniciados depois que a atualização for aplicada.</span><span class="sxs-lookup"><span data-stu-id="4c240-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="4c240-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c240-113">Remarks</span></span>

<span data-ttu-id="4c240-114">A propriedade **MSIDISABLERMRESTART** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c240-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c240-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c240-115">Requirements</span></span>



| <span data-ttu-id="4c240-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c240-116">Requirement</span></span> | <span data-ttu-id="4c240-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4c240-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c240-118">Versão</span><span class="sxs-lookup"><span data-stu-id="4c240-118">Version</span></span><br/> | <span data-ttu-id="4c240-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4c240-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4c240-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c240-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4c240-121">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4c240-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c240-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c240-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c240-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c240-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4c240-124">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4c240-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
