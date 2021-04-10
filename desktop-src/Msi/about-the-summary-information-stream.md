---
description: O fluxo de informações de Resumo contém informações sobre o pacote que podem ser exibidas por meio do Microsoft Windows Explorer.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Sobre o fluxo de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091551"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="506ac-103">Sobre o fluxo de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="506ac-103">About the Summary Information Stream</span></span>

<span data-ttu-id="506ac-104">O fluxo de informações de Resumo contém informações sobre o pacote que podem ser exibidas por meio do Microsoft Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="506ac-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="506ac-105">Essas informações podem ser acessadas por meio da interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="506ac-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="506ac-106">Cabe ao autor fornecer os valores para cada uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="506ac-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="506ac-107">O fluxo de informações de resumo usa COM para fornecer armazenamento estruturado de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="506ac-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="506ac-108">O COM dá suporte ao conceito de armazenamento estruturado acessível por meio da interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="506ac-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="506ac-109">O armazenamento estruturado, por sua vez, dá suporte ao conceito de conjuntos de propriedades como um método flexível para serialização de quase todas as informações.</span><span class="sxs-lookup"><span data-stu-id="506ac-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="506ac-110">A especificação COM define um único conjunto de propriedades padrão, informações resumidas, que é usado para popular folhas de propriedades visíveis no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="506ac-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="506ac-111">Portanto, as informações armazenadas no fluxo de informações de resumo podem ser exibidas pelos usuários quando clicam com o botão direito do mouse em um banco de dados do instalador ou em uma transformação e selecionam [Propriedades](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="506ac-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="506ac-112">Para obter uma lista do conjunto de propriedades de resumo, consulte [resumir informações de fluxo conjunto de propriedades](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="506ac-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="506ac-113">Para obter descrições breves das propriedades de informações resumidas usadas com bancos de dados, transformações e patches, consulte [descrições de propriedades de resumo](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="506ac-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



