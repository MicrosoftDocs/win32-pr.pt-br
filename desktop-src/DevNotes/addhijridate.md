---
description: '\\Painel de controle HKCU \\ internacional.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826234"
---
# <a name="addhijridate"></a><span data-ttu-id="995c6-103">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="995c6-103">AddHijriDate</span></span>

<span data-ttu-id="995c6-104">**\\Painel de controle HKCU \\ internacional**</span><span class="sxs-lookup"><span data-stu-id="995c6-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="995c6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="995c6-105">Data type</span></span> | <span data-ttu-id="995c6-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="995c6-106">Range</span></span>                      | <span data-ttu-id="995c6-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="995c6-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="995c6-108">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="995c6-108">REG\_SZ</span></span>   | <span data-ttu-id="995c6-109">*Um valor de ajuste válido*</span><span class="sxs-lookup"><span data-stu-id="995c6-109">*A valid adjustment value*</span></span> | <span data-ttu-id="995c6-110">(Nenhuma)</span><span class="sxs-lookup"><span data-stu-id="995c6-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="995c6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="995c6-111">Description</span></span>

<span data-ttu-id="995c6-112">Especifica os ajustes para a data dentro do calendário islâmico.</span><span class="sxs-lookup"><span data-stu-id="995c6-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="995c6-113">O calendário islâmico é um calendário lunar usado no mundo islâmico.</span><span class="sxs-lookup"><span data-stu-id="995c6-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="995c6-114">Os meses começam e terminam de acordo com um decree com base na observação da nova lua.</span><span class="sxs-lookup"><span data-stu-id="995c6-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="995c6-115">É difícil prever com precisão os inícios e finais dos meses, e há variações regionais, de modo que um ajuste entre zero e dois dias seja feito no calendário.</span><span class="sxs-lookup"><span data-stu-id="995c6-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="995c6-116">O valor do registro **AddHijriDate** armazena esse valor de ajuste da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="995c6-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="995c6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="995c6-117">Value</span></span>          | <span data-ttu-id="995c6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="995c6-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="995c6-119">AddHijriDate-2</span><span class="sxs-lookup"><span data-stu-id="995c6-119">AddHijriDate-2</span></span> | <span data-ttu-id="995c6-120">Subtraia dois dias.</span><span class="sxs-lookup"><span data-stu-id="995c6-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="995c6-121">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="995c6-121">AddHijriDate</span></span>   | <span data-ttu-id="995c6-122">Subtrair um dia.</span><span class="sxs-lookup"><span data-stu-id="995c6-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="995c6-123">(blank)</span><span class="sxs-lookup"><span data-stu-id="995c6-123">(blank)</span></span>        | <span data-ttu-id="995c6-124">Nenhum ajuste é necessário.</span><span class="sxs-lookup"><span data-stu-id="995c6-124">No adjustment is necessary.</span></span> <span data-ttu-id="995c6-125">(Se a data não tiver sido ajustada, essa entrada não aparecerá no registro.</span><span class="sxs-lookup"><span data-stu-id="995c6-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="995c6-126">Se a data tiver sido ajustada e restaurada para seu valor original, essa entrada aparecerá no registro sem valor.)</span><span class="sxs-lookup"><span data-stu-id="995c6-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="995c6-127">AddHijriDate + 1</span><span class="sxs-lookup"><span data-stu-id="995c6-127">AddHijriDate+1</span></span> | <span data-ttu-id="995c6-128">Adicionar um dia.</span><span class="sxs-lookup"><span data-stu-id="995c6-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="995c6-129">AddHijriDate + 2</span><span class="sxs-lookup"><span data-stu-id="995c6-129">AddHijriDate+2</span></span> | <span data-ttu-id="995c6-130">Adicione dois dias.</span><span class="sxs-lookup"><span data-stu-id="995c6-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="995c6-131">Essa entrada não existe no Registro por padrão.</span><span class="sxs-lookup"><span data-stu-id="995c6-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="995c6-132">Você pode adicioná-lo usando o editor do registro Regedit.exe ou usando o método de alteração descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="995c6-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="995c6-133">Alterar Método</span><span class="sxs-lookup"><span data-stu-id="995c6-133">Change Method</span></span>

<span data-ttu-id="995c6-134">Para alterar o valor dessa entrada ou adicioná-la ao registro, primeiro instale os arquivos para os idiomas de script complexo e da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="995c6-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="995c6-135">No painel de controle, clique em **Opções regionais e de idioma** e clique na guia **idiomas** . Em **suporte a idioma suplementar**, marque a caixa de seleção para **instalar arquivos para scripts complexos e idiomas da direita para a esquerda (incluindo tailandês)**.</span><span class="sxs-lookup"><span data-stu-id="995c6-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="995c6-136">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="995c6-136">Click **OK**.</span></span>

<span data-ttu-id="995c6-137">Para alterar o valor dessa entrada ou adicioná-la ao registro, no painel de controle, clique em **Opções regionais e de idioma**.</span><span class="sxs-lookup"><span data-stu-id="995c6-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="995c6-138">No campo **padrões e formatos** , selecione uma localidade que usa o calendário islâmico.</span><span class="sxs-lookup"><span data-stu-id="995c6-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="995c6-139">Clique no botão **Personalizar** e, em seguida, clique na guia **Data** . Na lista suspensa **Ajustar data do Hijri para:** , selecione o valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="995c6-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="995c6-140">Clique em **OK** e em **OK** novamente.</span><span class="sxs-lookup"><span data-stu-id="995c6-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="995c6-141">Método de ativação</span><span class="sxs-lookup"><span data-stu-id="995c6-141">Activation Method</span></span>

<span data-ttu-id="995c6-142">As alterações nessa entrada feitas por meio do painel de controle entram em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="995c6-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



