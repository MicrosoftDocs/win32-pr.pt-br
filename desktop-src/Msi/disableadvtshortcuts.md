---
description: A definição da propriedade DISABLEADVTSHORTCUTS desabilita a geração de atalhos que dão suporte à instalação sob demanda e ao anúncio. Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propriedade DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747982"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="37e5a-104">Propriedade DISABLEADVTSHORTCUTS</span><span class="sxs-lookup"><span data-stu-id="37e5a-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="37e5a-105">A definição da propriedade **DISABLEADVTSHORTCUTS** desabilita a geração de atalhos que dão suporte à [instalação sob demanda e ao](installation-on-demand.md) [anúncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="37e5a-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="37e5a-106">Definir essa propriedade especifica que esses atalhos devem ser substituídos por atalhos regulares.</span><span class="sxs-lookup"><span data-stu-id="37e5a-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="37e5a-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="37e5a-107">Default Value</span></span>

<span data-ttu-id="37e5a-108">Por padrão, a geração de atalhos de instalação sob demanda está habilitada.</span><span class="sxs-lookup"><span data-stu-id="37e5a-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="37e5a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="37e5a-109">Remarks</span></span>

<span data-ttu-id="37e5a-110">Os atalhos que dão suporte ao anúncio têm o nome de um recurso, em vez de um caminho de arquivo formatado do formato \[ \# FileKey \] , inseridos na coluna Target da [tabela de atalho](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="37e5a-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="37e5a-111">Se essa propriedade for definida e o recurso for instalado, o instalador gerará um atalho regular para o recurso.</span><span class="sxs-lookup"><span data-stu-id="37e5a-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="37e5a-112">Essa propriedade é normalmente usada por administradores para usuários que fazem roaming entre ambientes que não dão suporte a anúncios.</span><span class="sxs-lookup"><span data-stu-id="37e5a-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="37e5a-113">Essa propriedade pode ser definida por uma transformação, no fluxo administrativo ou na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="37e5a-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="37e5a-114">Se ele for definido usando a linha de comando ou por uma chamada para [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), ele deverá ser redefinido novamente durante cada instalação subsequente.</span><span class="sxs-lookup"><span data-stu-id="37e5a-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e5a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37e5a-115">Requirements</span></span>



| <span data-ttu-id="37e5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37e5a-116">Requirement</span></span> | <span data-ttu-id="37e5a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="37e5a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e5a-118">Versão</span><span class="sxs-lookup"><span data-stu-id="37e5a-118">Version</span></span><br/> | <span data-ttu-id="37e5a-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37e5a-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="37e5a-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37e5a-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="37e5a-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37e5a-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="37e5a-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="37e5a-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37e5a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="37e5a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e5a-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37e5a-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




