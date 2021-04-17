---
description: Se a propriedade LIMITUI for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propriedade LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782334"
---
# <a name="limitui-property"></a><span data-ttu-id="bad36-103">Propriedade LIMITUI</span><span class="sxs-lookup"><span data-stu-id="bad36-103">LIMITUI property</span></span>

<span data-ttu-id="bad36-104">Se a propriedade **LIMITUI** for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.</span><span class="sxs-lookup"><span data-stu-id="bad36-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="bad36-105">Essa propriedade é necessária em pacotes que não têm interface do usuário criada, mas que ainda contêm tabelas de interface do usuário, como a [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="bad36-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="bad36-106">Para obter uma descrição dos níveis de interface do usuário, consulte [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="bad36-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="bad36-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bad36-107">Remarks</span></span>

<span data-ttu-id="bad36-108">Os pacotes de instalação que contêm a propriedade **LIMITUI** também devem conter a propriedade [**ARPNOMODIFY**](arpnomodify.md) .</span><span class="sxs-lookup"><span data-stu-id="bad36-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="bad36-109">Isso é necessário para que um usuário obtenha o comportamento correto a partir de **Adicionar ou remover programas** no utilitário do **painel de controle** ao tentar configurar um produto.</span><span class="sxs-lookup"><span data-stu-id="bad36-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad36-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad36-110">Requirements</span></span>



| <span data-ttu-id="bad36-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad36-111">Requirement</span></span> | <span data-ttu-id="bad36-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bad36-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad36-113">Versão</span><span class="sxs-lookup"><span data-stu-id="bad36-113">Version</span></span><br/> | <span data-ttu-id="bad36-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bad36-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bad36-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bad36-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bad36-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bad36-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bad36-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bad36-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bad36-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bad36-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad36-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bad36-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bad36-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="bad36-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="bad36-121">**ARPNOMODIFY**</span><span class="sxs-lookup"><span data-stu-id="bad36-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




