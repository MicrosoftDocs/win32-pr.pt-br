---
description: Uma página de referência de evento (ERP) é um documento HTML que fornece Monitor de Rede informações sobre os eventos detectados durante a operação de monitor ou especialista.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Sobre páginas de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828564"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="a18f3-103">Sobre páginas de referência de evento</span><span class="sxs-lookup"><span data-stu-id="a18f3-103">About Event Reference Pages</span></span>

<span data-ttu-id="a18f3-104">Uma página de referência de evento (ERP) é um documento HTML que fornece Monitor de Rede informações sobre os eventos detectados durante a operação de monitor ou especialista.</span><span class="sxs-lookup"><span data-stu-id="a18f3-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="a18f3-105">Você pode exibir ERPs na Visualizador de Eventos de Monitor de Rede, monitorar ferramenta de controle ou em qualquer navegador que ofereça suporte aos recursos HTML do Microsoft Internet Explorer versão 4, 1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a18f3-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="a18f3-106">Ou seja, você pode adicionar controles com suporte ou linguagens com script em seu ERP.</span><span class="sxs-lookup"><span data-stu-id="a18f3-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="a18f3-107">No entanto, ERPs só aparecerá se o especialista designar o documento HTML por nome.</span><span class="sxs-lookup"><span data-stu-id="a18f3-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="a18f3-108">Quando indicado corretamente, o ERP aparece no painel inferior quando o evento na Visualizador de Eventos é selecionado.</span><span class="sxs-lookup"><span data-stu-id="a18f3-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="a18f3-109">A figura a seguir mostra um ERP associado ao monitor de intervalo de IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="a18f3-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![um ERP associado ao monitor de intervalo de IP](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="a18f3-111">Eventos de especialistas</span><span class="sxs-lookup"><span data-stu-id="a18f3-111">Expert Events</span></span>

<span data-ttu-id="a18f3-112">Os eventos de especialista são identificados pelo membro **EventIdent** de uma estrutura [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a18f3-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="a18f3-113">Ao escrever um especialista, você determina os valores de **EventIdent** , que normalmente são numerados 1, 2, 3 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a18f3-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="a18f3-114">Por exemplo, suponha que um especialista gere dois eventos (**EventIdent1** e **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="a18f3-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="a18f3-115">Se você quiser que o Visualizador de Eventos exiba os eventos separadamente, você deve criar dois documentos ERP separados.</span><span class="sxs-lookup"><span data-stu-id="a18f3-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 



