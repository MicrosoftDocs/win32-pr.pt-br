---
description: ICE51 verifica se um título foi fornecido para arquivos de recurso de fonte.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170841"
---
# <a name="ice51"></a><span data-ttu-id="bf62f-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="bf62f-103">ICE51</span></span>

<span data-ttu-id="bf62f-104">ICE51 verifica se um título foi fornecido para arquivos de recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="bf62f-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="bf62f-105">Você deve fornecer um título para um recurso de fonte que não tenha um nome inserido.</span><span class="sxs-lookup"><span data-stu-id="bf62f-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="bf62f-106">Somente os arquivos de recurso de fonte. TTC,. ttf e. otf não exigem um título, pois esses arquivos contêm um nome inserido.</span><span class="sxs-lookup"><span data-stu-id="bf62f-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="bf62f-107">Não forneça um título para um recurso de fonte que contenha um nome inserido porque o sistema registra a fonte duas vezes.</span><span class="sxs-lookup"><span data-stu-id="bf62f-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="bf62f-108">**[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** ICE51 não verifica os arquivos de recurso de fonte. otf.</span><span class="sxs-lookup"><span data-stu-id="bf62f-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="bf62f-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="bf62f-109">Result</span></span>

<span data-ttu-id="bf62f-110">ICE51 posta um erro se houver algum arquivo de recurso de fonte. TTC,. ttf e. otf com títulos.</span><span class="sxs-lookup"><span data-stu-id="bf62f-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="bf62f-111">ICE51 posta um aviso se houver outros arquivos de recurso de fonte sem título.</span><span class="sxs-lookup"><span data-stu-id="bf62f-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="bf62f-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf62f-112">Example</span></span>

<span data-ttu-id="bf62f-113">ICE51 relataria o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="bf62f-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="bf62f-114">ICE51 relataria a seguinte mensagem de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="bf62f-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="bf62f-115">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="bf62f-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="bf62f-116">Arquivo</span><span class="sxs-lookup"><span data-stu-id="bf62f-116">File</span></span>  | <span data-ttu-id="bf62f-117">FileName</span><span class="sxs-lookup"><span data-stu-id="bf62f-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="bf62f-118">Font1</span><span class="sxs-lookup"><span data-stu-id="bf62f-118">Font1</span></span> | <span data-ttu-id="bf62f-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="bf62f-119">font1.ttf</span></span> |
| <span data-ttu-id="bf62f-120">Font2</span><span class="sxs-lookup"><span data-stu-id="bf62f-120">Font2</span></span> | <span data-ttu-id="bf62f-121">font2. Fon</span><span class="sxs-lookup"><span data-stu-id="bf62f-121">font2.fon</span></span> |



 

[<span data-ttu-id="bf62f-122">Tabela de fontes</span><span class="sxs-lookup"><span data-stu-id="bf62f-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="bf62f-123">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="bf62f-123">File\_</span></span> | <span data-ttu-id="bf62f-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="bf62f-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="bf62f-125">Font1</span><span class="sxs-lookup"><span data-stu-id="bf62f-125">Font1</span></span>  | <span data-ttu-id="bf62f-126">Uma fonte realmente interessante</span><span class="sxs-lookup"><span data-stu-id="bf62f-126">A Really Cool Font</span></span> |
| <span data-ttu-id="bf62f-127">Font2</span><span class="sxs-lookup"><span data-stu-id="bf62f-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="bf62f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf62f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf62f-129">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="bf62f-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



