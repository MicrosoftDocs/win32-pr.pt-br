---
title: Exemplo de propriedade
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Saiba mais sobre: exemplo de propriedade'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088930"
---
# <a name="property-sample"></a><span data-ttu-id="16cbf-103">Exemplo de propriedade</span><span class="sxs-lookup"><span data-stu-id="16cbf-103">Property Sample</span></span>

<span data-ttu-id="16cbf-104">Este tópico descreve o exemplo de código de exemplo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="16cbf-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="16cbf-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="16cbf-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="16cbf-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="16cbf-106">Description</span></span>](#description)
-   [<span data-ttu-id="16cbf-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="16cbf-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="16cbf-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="16cbf-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="16cbf-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="16cbf-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="16cbf-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16cbf-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="16cbf-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="16cbf-111">Description</span></span>

<span data-ttu-id="16cbf-112">O exemplo de propriedade mostra como implementar três estilos diferentes de folhas de propriedades: modal, sem janela restrita e assistente.</span><span class="sxs-lookup"><span data-stu-id="16cbf-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="16cbf-113">Ele também mostra como usar a função [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) para modificar a caixa de diálogo da folha de propriedades antes ou depois de criada.</span><span class="sxs-lookup"><span data-stu-id="16cbf-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="16cbf-114">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="16cbf-114">Minimum Requirements</span></span>



| <span data-ttu-id="16cbf-115">Produto</span><span class="sxs-lookup"><span data-stu-id="16cbf-115">Product</span></span>          | <span data-ttu-id="16cbf-116">Versão</span><span class="sxs-lookup"><span data-stu-id="16cbf-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="16cbf-117">DLL</span><span class="sxs-lookup"><span data-stu-id="16cbf-117">DLL</span></span>              | <span data-ttu-id="16cbf-118">comctl32.dll versão 4,0</span><span class="sxs-lookup"><span data-stu-id="16cbf-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="16cbf-119">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="16cbf-119">Operating System</span></span> | <span data-ttu-id="16cbf-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="16cbf-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="16cbf-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="16cbf-121">Downloading the Sample</span></span>

<span data-ttu-id="16cbf-122">O exemplo de propriedade é instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx) e está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="16cbf-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="16cbf-123">Local</span><span class="sxs-lookup"><span data-stu-id="16cbf-123">Location</span></span>    | <span data-ttu-id="16cbf-124">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="16cbf-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cbf-125">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="16cbf-125">Windows SDK</span></span> | <span data-ttu-id="16cbf-126">% Arquivos de programas% \\ Microsoft SDKs \\ Windows \\ \[ versão número \] \\ exemplos \\ WinUI controles de \\ \\ \\ Propriedade comuns</span><span class="sxs-lookup"><span data-stu-id="16cbf-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="16cbf-127">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="16cbf-127">Building the Sample</span></span>

<span data-ttu-id="16cbf-128">Para criar o exemplo usando o prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="16cbf-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="16cbf-129">Abra a janela do prompt de comando e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="16cbf-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="16cbf-130">Digite `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="16cbf-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="16cbf-131">Para criar o exemplo usando o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="16cbf-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="16cbf-132">Abra o Windows Explorer e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="16cbf-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="16cbf-133">Clique duas vezes no ícone do arquivo. vcproj para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="16cbf-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="16cbf-134">No menu **Compilar** , selecione **Compilar solução** para compilar a solução.</span><span class="sxs-lookup"><span data-stu-id="16cbf-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16cbf-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16cbf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16cbf-136">Sobre folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="16cbf-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




