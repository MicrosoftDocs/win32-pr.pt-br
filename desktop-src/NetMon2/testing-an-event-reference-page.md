---
description: A etapa final da criação de uma página de referência de evento (ERP) é testá-la.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Testando uma página de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779475"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="8ad71-103">Testando uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="8ad71-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="8ad71-104">A etapa final da criação de uma página de referência de evento (ERP) é testá-la.</span><span class="sxs-lookup"><span data-stu-id="8ad71-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="8ad71-105">Você pode testar um ERP exibindo o arquivo em um navegador HTML, como o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8ad71-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="8ad71-106">Ou, você pode instalar o ERP e sua DLL de especialistas para testá-lo para invocação de evento e exibi-lo no Visualizador de Eventos de Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="8ad71-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="8ad71-107">Exibindo ERPs que não têm nenhuma DLL</span><span class="sxs-lookup"><span data-stu-id="8ad71-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="8ad71-108">Para exibir o ERP concluído sem uma DLL de especialista instalada, abra o arquivo com um visualizador de HTML que dê suporte às fontes inseridas.</span><span class="sxs-lookup"><span data-stu-id="8ad71-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="8ad71-109">A ilustração a seguir mostra o exemplo de arquivo ERP descrito em [escrevendo um ERP](writing-an-event-reference-page.md) conforme ele é exibido usando o Microsoft Internet Explorer versão 4, 1.</span><span class="sxs-lookup"><span data-stu-id="8ad71-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![arquivo ERP de exemplo](images/ie-erp.png)

<span data-ttu-id="8ad71-111">Testando ERPs que têm uma DLL</span><span class="sxs-lookup"><span data-stu-id="8ad71-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="8ad71-112">Depois que os arquivos ERP e a DLL de [**especialista**](experts.md) forem criados, você poderá testar a funcionalidade completa do seu ERPs com monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="8ad71-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="8ad71-113">Supõe-se que a DLL está depurada e possa gerar eventos válidos.</span><span class="sxs-lookup"><span data-stu-id="8ad71-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="8ad71-114">**Para testar ERPs que têm uma DLL**</span><span class="sxs-lookup"><span data-stu-id="8ad71-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="8ad71-115">Verifique se a DLL de especialista correta está instalada no diretório apropriado.</span><span class="sxs-lookup"><span data-stu-id="8ad71-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="8ad71-116">Para obter mais informações, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="8ad71-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="8ad71-117">Verifique o [nome correto](naming-an-event-reference-page.md) do arquivo ERP.</span><span class="sxs-lookup"><span data-stu-id="8ad71-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="8ad71-118">Verifique o [local correto](installing-existing-erps-to-network-monitor-2-1.md) do ERPs no diretório monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="8ad71-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="8ad71-119">ERPs expert de teste na interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="8ad71-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="8ad71-120">Gerar um evento de teste.</span><span class="sxs-lookup"><span data-stu-id="8ad71-120">Generate a test event.</span></span>
6.  <span data-ttu-id="8ad71-121">Verifique se o ERP aparece na Visualizador de Eventos de Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="8ad71-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="8ad71-122">Para obter mais informações sobre como criar um ERP, consulte:</span><span class="sxs-lookup"><span data-stu-id="8ad71-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="8ad71-123">Criando páginas de referência de evento expert e monitor</span><span class="sxs-lookup"><span data-stu-id="8ad71-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="8ad71-124">Escrevendo uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="8ad71-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="8ad71-125">Nomeando uma página de referência de evento</span><span class="sxs-lookup"><span data-stu-id="8ad71-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



