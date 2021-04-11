---
title: Exemplo de CustomAccServer
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365663"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="65c0d-103">Exemplo de CustomAccServer</span><span class="sxs-lookup"><span data-stu-id="65c0d-103">CustomAccServer Sample</span></span>

<span data-ttu-id="65c0d-104">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="65c0d-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="65c0d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="65c0d-105">Description</span></span>](#description)
-   [<span data-ttu-id="65c0d-106">Informações de download</span><span class="sxs-lookup"><span data-stu-id="65c0d-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="65c0d-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="65c0d-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="65c0d-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="65c0d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="65c0d-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="65c0d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="65c0d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c0d-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="65c0d-111">Description</span><span class="sxs-lookup"><span data-stu-id="65c0d-111">Description</span></span>

<span data-ttu-id="65c0d-112">Este exemplo mostra como implementar um Microsoft Acessibilidade Ativa Server para um controle personalizado simples.</span><span class="sxs-lookup"><span data-stu-id="65c0d-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="65c0d-113">O objeto acessível para o controle consiste no elemento raiz (uma caixa de listagem) e seus filhos (os itens de lista).</span><span class="sxs-lookup"><span data-stu-id="65c0d-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="65c0d-114">Informações de download</span><span class="sxs-lookup"><span data-stu-id="65c0d-114">Download Information</span></span>

<span data-ttu-id="65c0d-115">O exemplo CustomAccServer é instalado como parte do [SDK (Software Development Kit) do Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) e está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="65c0d-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="65c0d-116">Local</span><span class="sxs-lookup"><span data-stu-id="65c0d-116">Location</span></span>    | <span data-ttu-id="65c0d-117">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="65c0d-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65c0d-118">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="65c0d-118">Windows SDK</span></span> | <span data-ttu-id="65c0d-119">% Arquivos de programas% \\ Microsoft SDKs \\ Windows número de \\ \[ versão \] \\ amostras \\ WinUI \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="65c0d-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="65c0d-120">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="65c0d-120">Minimum Requirements</span></span>



| <span data-ttu-id="65c0d-121">Produto</span><span class="sxs-lookup"><span data-stu-id="65c0d-121">Product</span></span>          | <span data-ttu-id="65c0d-122">Versão</span><span class="sxs-lookup"><span data-stu-id="65c0d-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="65c0d-123">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="65c0d-123">Operating System</span></span> | <span data-ttu-id="65c0d-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65c0d-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="65c0d-125">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="65c0d-125">Windows SDK</span></span>      | <span data-ttu-id="65c0d-126">7.0</span><span class="sxs-lookup"><span data-stu-id="65c0d-126">7.0</span></span>                             |
| <span data-ttu-id="65c0d-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="65c0d-127">Visual Studio</span></span>    | <span data-ttu-id="65c0d-128">2008</span><span class="sxs-lookup"><span data-stu-id="65c0d-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="65c0d-129">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="65c0d-129">Building the Sample</span></span>

<span data-ttu-id="65c0d-130">Para criar o exemplo usando o Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="65c0d-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="65c0d-131">Execute a ferramenta de configuração do SDK (Software Development Kit) do Microsoft Windows fornecida com o SDK para adicionar diretórios de inclusão do SDK ao Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="65c0d-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="65c0d-132">Abra o Windows Explorer e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="65c0d-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="65c0d-133">Clique duas vezes no ícone do arquivo. sln (solução) para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="65c0d-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="65c0d-134">No menu **Compilar** , selecione **Compilar solução** para compilar a solução.</span><span class="sxs-lookup"><span data-stu-id="65c0d-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="65c0d-135">O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.</span><span class="sxs-lookup"><span data-stu-id="65c0d-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="65c0d-136">Para criar o exemplo na linha de comando, consulte Criando exemplos no SDK do Windows notas de versão no seguinte local:% Arquivos de programas% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="65c0d-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="65c0d-137">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="65c0d-137">Running the Sample</span></span>

<span data-ttu-id="65c0d-138">Para executar o exemplo:</span><span class="sxs-lookup"><span data-stu-id="65c0d-138">To run the sample:</span></span>

1.  <span data-ttu-id="65c0d-139">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="65c0d-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="65c0d-140">Digite AccServer.exe na linha de comando ou clique duas vezes no ícone de AccServer.exe para iniciá-lo no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="65c0d-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="65c0d-141">Para executar a partir do Visual Studio, pressione F5 ou clique em **Iniciar Depuração** no menu **depurar** .</span><span class="sxs-lookup"><span data-stu-id="65c0d-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65c0d-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c0d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c0d-143">Amostras</span><span class="sxs-lookup"><span data-stu-id="65c0d-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




