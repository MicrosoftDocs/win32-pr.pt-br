---
description: Definir a propriedade DISABLEMEDIA impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto. No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propriedade DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750828"
---
# <a name="disablemedia-property"></a><span data-ttu-id="06893-104">Propriedade DISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="06893-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="06893-105">Definir a propriedade [**DISABLEMEDIA**](disablemedia.md) impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.</span><span class="sxs-lookup"><span data-stu-id="06893-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="06893-106">No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="06893-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="06893-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="06893-107">Remarks</span></span>

<span data-ttu-id="06893-108">Observe que a propriedade [**DISABLEMEDIA**](disablemedia.md) tem um efeito diferente de definir a política DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="06893-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="06893-109">A definição de **DISABLEMEDIA** impede o registro de qualquer fonte de mídia, e isso também impede a primeira instalação de um aplicativo de fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="06893-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="06893-110">Para obter detalhes sobre como proteger as fontes de mídia do [*aplicativo gerenciado*](m-gly.md) em busca e instalação por usuários não administrativos, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="06893-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06893-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06893-111">Requirements</span></span>



| <span data-ttu-id="06893-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="06893-112">Requirement</span></span> | <span data-ttu-id="06893-113">Valor</span><span class="sxs-lookup"><span data-stu-id="06893-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06893-114">Versão</span><span class="sxs-lookup"><span data-stu-id="06893-114">Version</span></span><br/> | <span data-ttu-id="06893-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="06893-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="06893-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="06893-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="06893-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06893-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="06893-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="06893-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06893-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="06893-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06893-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06893-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




