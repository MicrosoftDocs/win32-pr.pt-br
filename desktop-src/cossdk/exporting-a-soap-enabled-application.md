---
description: Quando você usa o COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou mesmo Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportando um aplicativo SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826516"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="3d04f-103">Exportando um aplicativo SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="3d04f-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="3d04f-104">Quando você usa o COM+ para criar um serviço Web XML, esse serviço pode ser usado por qualquer cliente autorizado, incluindo aqueles que não usam COM+ ou mesmo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3d04f-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="3d04f-105">No entanto, usar um serviço Web COM+ no modo CAO (objeto ativado pelo cliente) de um aplicativo cliente do COM+ é especialmente fácil.</span><span class="sxs-lookup"><span data-stu-id="3d04f-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="3d04f-106">Basta exportar o aplicativo habilitado para SOAP no modo proxy e, em seguida, [importá](importing-a-soap-enabled-application.md) -lo para o cliente para o qual você deseja acessar o Web Service XML correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d04f-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3d04f-107">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="3d04f-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="3d04f-108">Para exportar um aplicativo habilitado para SOAP de um servidor, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3d04f-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="3d04f-109">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3d04f-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="3d04f-110">Clique com o botão direito do mouse no componente que você deseja expor como um serviço Web XML e escolha **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="3d04f-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="3d04f-111">O **Assistente para exportação de aplicativos com+** é exibido.</span><span class="sxs-lookup"><span data-stu-id="3d04f-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="3d04f-112">Na caixa de texto rotulada, **Insira o caminho completo e o nome do arquivo do aplicativo a ser criado**, insira o caminho completo e o nome do arquivo do MSI que conterá o aplicativo exportado ou clique em **procurar** para selecionar o caminho completo e o nome do arquivo usando uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3d04f-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="3d04f-113">Em **exportar como**, selecione o botão de opção **proxy de aplicativo – instalar em outros computadores para habilitar o acesso a este computador** .</span><span class="sxs-lookup"><span data-stu-id="3d04f-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3d04f-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3d04f-114">Visual Basic</span></span>

<span data-ttu-id="3d04f-115">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="3d04f-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3d04f-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="3d04f-116">C/C++</span></span>

<span data-ttu-id="3d04f-117">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="3d04f-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d04f-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d04f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d04f-119">Visão geral do serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="3d04f-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="3d04f-120">Criando Serviços Web XML</span><span class="sxs-lookup"><span data-stu-id="3d04f-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="3d04f-121">Importando um aplicativo SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="3d04f-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



