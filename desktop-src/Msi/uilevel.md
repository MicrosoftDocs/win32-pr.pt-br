---
description: O instalador define a propriedade UILevel para o nível da interface do usuário.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propriedade UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768714"
---
# <a name="uilevel-property"></a><span data-ttu-id="43569-103">Propriedade UILevel</span><span class="sxs-lookup"><span data-stu-id="43569-103">UILevel property</span></span>

<span data-ttu-id="43569-104">O instalador define a propriedade **UILevel** para o nível da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="43569-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="43569-105">A interface do usuário interna é habilitada e definida por [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="43569-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="43569-106">Essa propriedade é definida como um dos seguintes tipos de dados INSTALLUILEVEL.</span><span class="sxs-lookup"><span data-stu-id="43569-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="43569-107">INSTALLUILEVEL</span><span class="sxs-lookup"><span data-stu-id="43569-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="43569-108">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="43569-108">Numeric value</span></span> | <span data-ttu-id="43569-109">Nível da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="43569-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="43569-110">INSTALLUILEVEL \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="43569-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="43569-111">2</span><span class="sxs-lookup"><span data-stu-id="43569-111">2</span></span>             | <span data-ttu-id="43569-112">Instalação Totalmente Silenciosa.</span><span class="sxs-lookup"><span data-stu-id="43569-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="43569-113">INSTALLUILEVEL \_ básico</span><span class="sxs-lookup"><span data-stu-id="43569-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="43569-114">3</span><span class="sxs-lookup"><span data-stu-id="43569-114">3</span></span>             | <span data-ttu-id="43569-115">Progresso simples e tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="43569-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="43569-116">INSTALLUILEVEL \_ reduzido</span><span class="sxs-lookup"><span data-stu-id="43569-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="43569-117">4</span><span class="sxs-lookup"><span data-stu-id="43569-117">4</span></span>             | <span data-ttu-id="43569-118">Interface do usuário criada, caixas de diálogo do assistente suprimidas.</span><span class="sxs-lookup"><span data-stu-id="43569-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="43569-119">INSTALLUILEVEL \_ completo</span><span class="sxs-lookup"><span data-stu-id="43569-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="43569-120">5</span><span class="sxs-lookup"><span data-stu-id="43569-120">5</span></span>             | <span data-ttu-id="43569-121">IU criada com assistentes, progresso, erros.</span><span class="sxs-lookup"><span data-stu-id="43569-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="43569-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43569-122">Requirements</span></span>



| <span data-ttu-id="43569-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="43569-123">Requirement</span></span> | <span data-ttu-id="43569-124">Valor</span><span class="sxs-lookup"><span data-stu-id="43569-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43569-125">Versão</span><span class="sxs-lookup"><span data-stu-id="43569-125">Version</span></span><br/> | <span data-ttu-id="43569-126">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="43569-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="43569-127">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="43569-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="43569-128">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="43569-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="43569-129">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="43569-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43569-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="43569-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43569-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43569-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="43569-132">Interface do usuário</span><span class="sxs-lookup"><span data-stu-id="43569-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="43569-133">Determinando o nível da interface do usuário de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="43569-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




