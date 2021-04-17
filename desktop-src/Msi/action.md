---
description: A propriedade ACTION pode ser definida com os valores a seguir.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Propriedade de ação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749806"
---
# <a name="action-property"></a><span data-ttu-id="2d85c-103">Propriedade de ação</span><span class="sxs-lookup"><span data-stu-id="2d85c-103">ACTION property</span></span>

<span data-ttu-id="2d85c-104">A propriedade **Action** pode ser definida com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d85c-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="2d85c-105">Valor</span><span class="sxs-lookup"><span data-stu-id="2d85c-105">Value</span></span>



| <span data-ttu-id="2d85c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="2d85c-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="2d85c-107">Significado</span><span class="sxs-lookup"><span data-stu-id="2d85c-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="2d85c-108"><dt>**PRÉ-instalação**</dt></span><span class="sxs-lookup"><span data-stu-id="2d85c-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="2d85c-109">Ação de instalação</span><span class="sxs-lookup"><span data-stu-id="2d85c-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="2d85c-110"><dt>**ANUNCI**</dt></span><span class="sxs-lookup"><span data-stu-id="2d85c-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="2d85c-111">Ação de anúncio</span><span class="sxs-lookup"><span data-stu-id="2d85c-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="2d85c-112"><dt>**ADM**</dt></span><span class="sxs-lookup"><span data-stu-id="2d85c-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="2d85c-113">Ação de administrador</span><span class="sxs-lookup"><span data-stu-id="2d85c-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="2d85c-114">A propriedade **Action** determina qual ação executar se um nome de ação nulo for fornecido para [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou para o [**método DoAction**](session-doaction.md).</span><span class="sxs-lookup"><span data-stu-id="2d85c-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="2d85c-115">Se nenhum valor for definido para a propriedade **Action** , o instalador chamará a [ação de instalação](install-action.md).</span><span class="sxs-lookup"><span data-stu-id="2d85c-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d85c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d85c-116">Requirements</span></span>



| <span data-ttu-id="2d85c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d85c-117">Requirement</span></span> | <span data-ttu-id="2d85c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2d85c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d85c-119">Versão</span><span class="sxs-lookup"><span data-stu-id="2d85c-119">Version</span></span><br/> | <span data-ttu-id="2d85c-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d85c-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d85c-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d85c-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d85c-122">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2d85c-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2d85c-123">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2d85c-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d85c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d85c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d85c-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d85c-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




