---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcadores
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- marcadores, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823006"
---
# <a name="markers"></a><span data-ttu-id="d20fb-107">Marcadores</span><span class="sxs-lookup"><span data-stu-id="d20fb-107">Markers</span></span>

<span data-ttu-id="d20fb-108">Os marcadores são chamados de locais na linha do tempo de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d20fb-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="d20fb-109">Cada marcador tem um nome e um tempo de apresentação que você atribui.</span><span class="sxs-lookup"><span data-stu-id="d20fb-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="d20fb-110">Você pode especificar quantos marcadores forem necessários para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d20fb-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="d20fb-111">Os marcadores são úteis para dividir arquivos ASF grandes em partes lógicas.</span><span class="sxs-lookup"><span data-stu-id="d20fb-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="d20fb-112">Um aplicativo que usa o objeto leitor para reproduzir arquivos ASF pode fornecer ao usuário a opção de ignorar o marcador para o marcador, simplificando a navegação da mídia digital.</span><span class="sxs-lookup"><span data-stu-id="d20fb-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="d20fb-113">Por exemplo, se você estiver fazendo um arquivo ASF de uma apresentação, poderá colocar marcadores na linha do tempo para cada tópico principal que é discutido.</span><span class="sxs-lookup"><span data-stu-id="d20fb-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="d20fb-114">Na reprodução, em vez de obter uma linha do tempo longa e ter de adivinhar no local para o qual buscar, um usuário pode simplesmente escolher um tópico de uma lista e ir direto para a parte pertinente do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d20fb-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="d20fb-115">Os marcadores são manipulados pelo objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="d20fb-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="d20fb-116">Você pode adicionar, remover e exibir os marcadores em um arquivo a qualquer momento depois que o arquivo tiver sido gravado.</span><span class="sxs-lookup"><span data-stu-id="d20fb-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d20fb-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d20fb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d20fb-118">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="d20fb-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="d20fb-119">**Para buscar marcadores**</span><span class="sxs-lookup"><span data-stu-id="d20fb-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="d20fb-120">**Usando marcadores**</span><span class="sxs-lookup"><span data-stu-id="d20fb-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




