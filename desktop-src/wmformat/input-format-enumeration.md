---
title: Enumeração de formato de entrada
description: Enumeração de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- SDK do Windows Media Format, enumerações de formato de entrada
- SDK do Windows Media Format, enumerando formatos de entrada
- ASF (Advanced Systems Format), enumerações de formato de entrada
- ASF (formato de sistemas avançados), enumerações de formato de entrada
- Formato de sistema avançado (ASF), enumerando formatos de entrada
- ASF (formato de sistemas avançados), enumerando formatos de entrada
- enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453709"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="20a9e-110">Enumeração de formato de entrada</span><span class="sxs-lookup"><span data-stu-id="20a9e-110">Input Format Enumeration</span></span>

<span data-ttu-id="20a9e-111">O objeto Writer Obtém informações de formato de fluxo do perfil que você fornece.</span><span class="sxs-lookup"><span data-stu-id="20a9e-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="20a9e-112">As informações de configuração de fluxo em um perfil fornecem ao escritor todas as informações necessárias sobre como os dados devem ser gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="20a9e-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="20a9e-113">O perfil não fornece ao gravador nenhuma informação sobre o formato dos exemplos de entrada que seu aplicativo fornece.</span><span class="sxs-lookup"><span data-stu-id="20a9e-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="20a9e-114">Os formatos de entrada serão desconhecidos somente para fluxos compactados com um dos codecs de mídia do Windows; as entradas para tipos de fluxo arbitrários são previsíveis com base nas informações no perfil.</span><span class="sxs-lookup"><span data-stu-id="20a9e-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="20a9e-115">O objeto Writer pode se comunicar com o codec de um fluxo para determinar os tipos de entrada que podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="20a9e-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="20a9e-116">Os métodos são fornecidos para enumerar os tipos de entrada possíveis.</span><span class="sxs-lookup"><span data-stu-id="20a9e-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="20a9e-117">Você sempre deve encontrar o tipo de entrada que corresponde à sua mídia de entrada enumerando os tipos com suporte em vez de definir as propriedades de mídia de entrada manualmente.</span><span class="sxs-lookup"><span data-stu-id="20a9e-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="20a9e-118">Para obter mais informações, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="20a9e-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20a9e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20a9e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20a9e-120">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="20a9e-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="20a9e-121">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="20a9e-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




