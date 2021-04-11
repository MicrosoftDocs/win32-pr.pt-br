---
title: Licenças
description: Licenças
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292766"
---
# <a name="licenses"></a><span data-ttu-id="94868-111">Licenças</span><span class="sxs-lookup"><span data-stu-id="94868-111">Licenses</span></span>

<span data-ttu-id="94868-112">Uma licença é um conjunto de dados que descreve as condições sob as quais os dados nos arquivos protegidos podem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="94868-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="94868-113">Cada licença se aplica a um identificador de chave, que normalmente é atribuído a um único arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="94868-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="94868-114">Esse identificador é usado para identificar o conteúdo protegido na licença.</span><span class="sxs-lookup"><span data-stu-id="94868-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="94868-115">Cada licença especifica uma ou mais ações que podem ser executadas com o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="94868-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="94868-116">Essas ações, também chamadas de direitos, podem ser limitadas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="94868-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="94868-117">Ao combinar datas de início, datas de término, contagens e limites de tempo, o emissor da licença pode criar quase qualquer limitação imaginar à direita.</span><span class="sxs-lookup"><span data-stu-id="94868-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="94868-118">As licenças são emitidas por um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="94868-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="94868-119">Quando uma licença é adquirida, ela é armazenada no computador cliente no armazenamento de licença local, que é um arquivo protegido que contém licenças e outros dados de DRM.</span><span class="sxs-lookup"><span data-stu-id="94868-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="94868-120">Quando o conteúdo protegido é acessado por um aplicativo, o subsistema DRM pesquisa o repositório de licenças local para uma licença que concede o direito apropriado.</span><span class="sxs-lookup"><span data-stu-id="94868-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="94868-121">Se nenhuma licença for encontrada, o aplicativo poderá adquirir uma com base nas informações armazenadas no cabeçalho DRM do arquivo.</span><span class="sxs-lookup"><span data-stu-id="94868-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="94868-122">Várias licenças podem ser emitidas para o mesmo arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="94868-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="94868-123">Quando o subsistema DRM determina se uma ação é permitida, ele agrega os direitos de todas as licenças que se aplicam.</span><span class="sxs-lookup"><span data-stu-id="94868-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="94868-124">Cada licença pode ser atribuída a uma prioridade.</span><span class="sxs-lookup"><span data-stu-id="94868-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="94868-125">Se mais de uma licença se aplicar a uma ação, a licença de prioridade mais alta será verificada para determinar se as contagens precisam ser decrementadas.</span><span class="sxs-lookup"><span data-stu-id="94868-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94868-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94868-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94868-127">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="94868-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




