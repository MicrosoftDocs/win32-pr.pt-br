---
description: A propriedade MSIRESTARTMANAGERCONTROL especifica se o pacote de Windows Installer usa a funcionalidade de caixa de diálogo do Gerenciador de reinicialização ou FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propriedade MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778719"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="c96cd-103">Propriedade MSIRESTARTMANAGERCONTROL</span><span class="sxs-lookup"><span data-stu-id="c96cd-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="c96cd-104">A propriedade **MSIRESTARTMANAGERCONTROL** especifica se o pacote de Windows Installer usa a funcionalidade de [caixa de diálogo](filesinuse-dialog.md) do Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) ou FilesInUse.</span><span class="sxs-lookup"><span data-stu-id="c96cd-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="c96cd-105">Valor</span><span class="sxs-lookup"><span data-stu-id="c96cd-105">Value</span></span>



| <span data-ttu-id="c96cd-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c96cd-106">Value</span></span>                                                                                        | <span data-ttu-id="c96cd-107">Significado</span><span class="sxs-lookup"><span data-stu-id="c96cd-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c96cd-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c96cd-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="c96cd-109">Esse será o valor padrão se a propriedade não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="c96cd-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="c96cd-110">Windows Installer sempre tenta usar o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c96cd-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c96cd-111"><dt>Desativar</dt></span><span class="sxs-lookup"><span data-stu-id="c96cd-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="c96cd-112">Desabilita a interação do pacote com o Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="c96cd-113">Windows Installer usa a [caixa de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="c96cd-114"><dt>"DisableShutdown"</dt></span><span class="sxs-lookup"><span data-stu-id="c96cd-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="c96cd-115">Windows Installer usa a [caixa de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="c96cd-116">Essa configuração desabilita as tentativas do Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) para atenuar as reinicializações ao instalar um pacote de Windows Installer que não foi criado para usar o Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="c96cd-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="c96cd-117">O instalador ainda usa o Gerenciador de reinicialização para detectar arquivos em uso pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c96cd-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c96cd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c96cd-118">Remarks</span></span>

<span data-ttu-id="c96cd-119">A propriedade **MSIRESTARTMANAGERCONTROL** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c96cd-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="c96cd-120">O valor dessa propriedade pode ser modificado usando transformações ou atualizações de personalização.</span><span class="sxs-lookup"><span data-stu-id="c96cd-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="c96cd-121">Alterar o valor dessa propriedade de ações personalizadas não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="c96cd-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c96cd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c96cd-122">Requirements</span></span>



| <span data-ttu-id="c96cd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c96cd-123">Requirement</span></span> | <span data-ttu-id="c96cd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c96cd-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96cd-125">Versão</span><span class="sxs-lookup"><span data-stu-id="c96cd-125">Version</span></span><br/> | <span data-ttu-id="c96cd-126">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c96cd-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c96cd-127">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c96cd-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c96cd-128">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c96cd-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c96cd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c96cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96cd-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c96cd-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c96cd-131">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="c96cd-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="c96cd-132">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="c96cd-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
