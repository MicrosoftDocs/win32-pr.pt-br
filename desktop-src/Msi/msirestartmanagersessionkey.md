---
description: O instalador define o valor da propriedade MsiRestartManagerSessionKey para a chave de sessão para a sessão do Gerenciador de reinicialização.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propriedade MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750799"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="419ac-103">Propriedade MsiRestartManagerSessionKey</span><span class="sxs-lookup"><span data-stu-id="419ac-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="419ac-104">O instalador define o valor da propriedade **MsiRestartManagerSessionKey** para a chave de sessão para a sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="419ac-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="419ac-105">As ações personalizadas podem usar a chave de sessão para ingressar na sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="419ac-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="419ac-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="419ac-106">Remarks</span></span>

<span data-ttu-id="419ac-107">O instalador define o valor da propriedade **MsiRestartManagerSessionKey** na inicialização e, em seguida, limpa o valor durante a ação [InstallValidate](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="419ac-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="419ac-108">Ações personalizadas que precisam do valor da propriedade **MsiRestartManagerSessionKey** devem vir antes da ação InstallValidate na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="419ac-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="419ac-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="419ac-109">Requirements</span></span>



| <span data-ttu-id="419ac-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="419ac-110">Requirement</span></span> | <span data-ttu-id="419ac-111">Valor</span><span class="sxs-lookup"><span data-stu-id="419ac-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419ac-112">Versão</span><span class="sxs-lookup"><span data-stu-id="419ac-112">Version</span></span><br/> | <span data-ttu-id="419ac-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="419ac-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="419ac-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="419ac-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="419ac-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="419ac-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="419ac-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="419ac-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419ac-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="419ac-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="419ac-118">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="419ac-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
