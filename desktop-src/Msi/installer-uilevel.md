---
description: A propriedade UILevel do objeto instalador é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes no espaço do processo atual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Propriedade Installer. UILevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747329"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="81b86-103">Propriedade Installer. UILevel</span><span class="sxs-lookup"><span data-stu-id="81b86-103">Installer.UILevel property</span></span>

<span data-ttu-id="81b86-104">A propriedade **UILevel** do objeto [**instalador**](installer-object.md) é uma propriedade de leitura/gravação que indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes no espaço do processo atual.</span><span class="sxs-lookup"><span data-stu-id="81b86-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="81b86-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81b86-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b86-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81b86-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="81b86-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="81b86-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="81b86-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="81b86-108">Remarks</span></span>



| <span data-ttu-id="81b86-109">Nível da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="81b86-109">User interface level</span></span>   | <span data-ttu-id="81b86-110">Valor</span><span class="sxs-lookup"><span data-stu-id="81b86-110">Value</span></span> | <span data-ttu-id="81b86-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="81b86-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b86-112">msiUILevelNoChange</span><span class="sxs-lookup"><span data-stu-id="81b86-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="81b86-113">0</span><span class="sxs-lookup"><span data-stu-id="81b86-113">0</span></span>     | <span data-ttu-id="81b86-114">Não altera o nível da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="81b86-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="81b86-115">msiUILevelDefault</span><span class="sxs-lookup"><span data-stu-id="81b86-115">msiUILevelDefault</span></span>      | <span data-ttu-id="81b86-116">1</span><span class="sxs-lookup"><span data-stu-id="81b86-116">1</span></span>     | <span data-ttu-id="81b86-117">Usa o nível de interface do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="81b86-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="81b86-118">msiUILevelNone</span><span class="sxs-lookup"><span data-stu-id="81b86-118">msiUILevelNone</span></span>         | <span data-ttu-id="81b86-119">2</span><span class="sxs-lookup"><span data-stu-id="81b86-119">2</span></span>     | <span data-ttu-id="81b86-120">Instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="81b86-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="81b86-121">msiUILevelBasic</span><span class="sxs-lookup"><span data-stu-id="81b86-121">msiUILevelBasic</span></span>        | <span data-ttu-id="81b86-122">3</span><span class="sxs-lookup"><span data-stu-id="81b86-122">3</span></span>     | <span data-ttu-id="81b86-123">Progresso simples e tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="81b86-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="81b86-124">msiUILevelReduced</span><span class="sxs-lookup"><span data-stu-id="81b86-124">msiUILevelReduced</span></span>      | <span data-ttu-id="81b86-125">4</span><span class="sxs-lookup"><span data-stu-id="81b86-125">4</span></span>     | <span data-ttu-id="81b86-126">Caixas de diálogo de interface do usuário e assistente criadas suprimidas.</span><span class="sxs-lookup"><span data-stu-id="81b86-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="81b86-127">msiUILevelFull</span><span class="sxs-lookup"><span data-stu-id="81b86-127">msiUILevelFull</span></span>         | <span data-ttu-id="81b86-128">5</span><span class="sxs-lookup"><span data-stu-id="81b86-128">5</span></span>     | <span data-ttu-id="81b86-129">IU criada com assistentes, progresso e erros.</span><span class="sxs-lookup"><span data-stu-id="81b86-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="81b86-130">msiUILevelHideCancel</span><span class="sxs-lookup"><span data-stu-id="81b86-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="81b86-131">32</span><span class="sxs-lookup"><span data-stu-id="81b86-131">32</span></span>    | <span data-ttu-id="81b86-132">Se combinado com o valor msiUILevelBasic, o instalador mostrará as caixas de diálogo de progresso, mas não exibirá um botão **Cancelar** na caixa de diálogo para impedir que os usuários cancelem a instalação.</span><span class="sxs-lookup"><span data-stu-id="81b86-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="81b86-133">msiUILevelProgressOnly</span><span class="sxs-lookup"><span data-stu-id="81b86-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="81b86-134">64</span><span class="sxs-lookup"><span data-stu-id="81b86-134">64</span></span>    | <span data-ttu-id="81b86-135">Se combinado com o valor msiUILevelBasic, o instalador exibirá as caixas de diálogo de progresso, mas não exibirá caixas de diálogo modais ou caixas de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="81b86-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="81b86-136">msiUILevelEndDialog</span><span class="sxs-lookup"><span data-stu-id="81b86-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="81b86-137">128</span><span class="sxs-lookup"><span data-stu-id="81b86-137">128</span></span>   | <span data-ttu-id="81b86-138">Se combinado com qualquer valor acima, o instalador exibirá uma caixa de diálogo modal no final de uma instalação bem-sucedida ou se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="81b86-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="81b86-139">Nenhuma caixa de diálogo será exibida se o usuário cancelar.</span><span class="sxs-lookup"><span data-stu-id="81b86-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="81b86-140">Consulte também, [determinando o nível da interface do usuário de uma ação personalizada](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="81b86-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81b86-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b86-141">Requirements</span></span>



| <span data-ttu-id="81b86-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b86-142">Requirement</span></span> | <span data-ttu-id="81b86-143">Valor</span><span class="sxs-lookup"><span data-stu-id="81b86-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b86-144">Versão</span><span class="sxs-lookup"><span data-stu-id="81b86-144">Version</span></span><br/> | <span data-ttu-id="81b86-145">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="81b86-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="81b86-146">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81b86-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="81b86-147">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="81b86-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="81b86-148">DLL</span><span class="sxs-lookup"><span data-stu-id="81b86-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="81b86-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b86-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="81b86-150">IID</span><span class="sxs-lookup"><span data-stu-id="81b86-150">IID</span></span><br/>     | <span data-ttu-id="81b86-151">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="81b86-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




