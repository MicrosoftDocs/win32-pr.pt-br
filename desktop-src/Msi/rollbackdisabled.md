---
description: O instalador define a propriedade RollbackDisabled quando a reversão foi desabilitada.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propriedade RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751839"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="37323-103">Propriedade RollbackDisabled</span><span class="sxs-lookup"><span data-stu-id="37323-103">RollbackDisabled property</span></span>

<span data-ttu-id="37323-104">O instalador define a propriedade **RollbackDisabled** quando a reversão foi desabilitada.</span><span class="sxs-lookup"><span data-stu-id="37323-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="37323-105">O **RollbackDisabled** é usado por autores de pacotes que precisam garantir que o instalador não tenha desabilitado a reversão.</span><span class="sxs-lookup"><span data-stu-id="37323-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="37323-106">A propriedade **RollbackDisabled** pode ser usada em uma expressão condicional que se recuse efetivamente a continuar com a instalação se a propriedade **RollbackDisabled** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="37323-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="37323-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="37323-107">Default Value</span></span>

<span data-ttu-id="37323-108">Por padrão, a reversão está habilitada.</span><span class="sxs-lookup"><span data-stu-id="37323-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="37323-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="37323-109">Remarks</span></span>

<span data-ttu-id="37323-110">Como a [reversão](rollback-custom-actions.md) e a [confirmação](commit-custom-actions.md) não são executadas enquanto a reversão está desabilitada, o instalador não pode instalar corretamente um pacote que usa esses tipos de ações personalizadas em uma transação durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="37323-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="37323-111">Nesse caso, o autor do pacote deve incluir uma condição usando DisableRollback que impedirá a instalação de continuar se a reversão estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="37323-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="37323-112">O valor da política DisableRollback pode ser definido por um administrador como parte da atribuição da política do sistema.</span><span class="sxs-lookup"><span data-stu-id="37323-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="37323-113">Os administradores são aconselhados a não desabilitar a reversão, a menos que necessário.</span><span class="sxs-lookup"><span data-stu-id="37323-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="37323-114">Para obter mais informações sobre o valor da política DisableRollback, consulte [política do sistema](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="37323-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37323-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37323-115">Requirements</span></span>



| <span data-ttu-id="37323-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37323-116">Requirement</span></span> | <span data-ttu-id="37323-117">Valor</span><span class="sxs-lookup"><span data-stu-id="37323-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37323-118">Versão</span><span class="sxs-lookup"><span data-stu-id="37323-118">Version</span></span><br/> | <span data-ttu-id="37323-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37323-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="37323-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37323-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="37323-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37323-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="37323-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="37323-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37323-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="37323-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37323-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37323-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="37323-125">Reverter instalação</span><span class="sxs-lookup"><span data-stu-id="37323-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="37323-126">Política do sistema</span><span class="sxs-lookup"><span data-stu-id="37323-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="37323-127">reverter ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="37323-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="37323-128">confirmar ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="37323-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




