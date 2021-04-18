---
title: Para adicionar dados de script ao cabeçalho
description: Para adicionar dados de script ao cabeçalho
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- SDK do Windows Media Format, adicionando dados de script aos cabeçalhos
- ASF (Advanced Systems Format), adicionando dados de script aos cabeçalhos
- ASF (formato de sistemas avançados), adicionando dados de script aos cabeçalhos
- scripts, adicionando dados aos cabeçalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105786153"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="2dbcb-107">Para adicionar dados de script ao cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2dbcb-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="2dbcb-108">Você pode incluir comandos de script no cabeçalho de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="2dbcb-109">Para gravar comandos de script no cabeçalho no momento da codificação, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="2dbcb-110">Execute estas etapas antes de chamar [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="2dbcb-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="2dbcb-111">Obtenha um ponteiro para a interface **IWMHeaderInfo** chamando **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="2dbcb-112">Adicione cada comando de script desejado chamando [**IWMHeaderInfo:: addScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span><span class="sxs-lookup"><span data-stu-id="2dbcb-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="2dbcb-113">Cada chamada usa as duas cadeias de caracteres separadamente e o tempo de apresentação a ser usado para o comando como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="2dbcb-114">Quando um aplicativo lê o arquivo, ele precisa recuperar todos os comandos de script.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="2dbcb-115">Para localizar todos os comandos de script no cabeçalho de um arquivo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="2dbcb-116">Isso deve ser feito antes de iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="2dbcb-117">Obtenha um ponteiro para a interface **IWMHeaderInfo** do objeto leitor (ou objeto leitor síncrono) chamando o método **QueryInterface** de outra interface no objeto.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="2dbcb-118">Obtenha o número total de scripts no cabeçalho chamando [**IWMHeaderInfo:: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span><span class="sxs-lookup"><span data-stu-id="2dbcb-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="2dbcb-119">Execute um loop por todos os scripts no cabeçalho, um de cada vez, usando chamadas para [**IWMHeaderInfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="2dbcb-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="2dbcb-120">Crie uma lista das horas de apresentação para que seu aplicativo possa reagir aos comandos no momento apropriado.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="2dbcb-121">Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um horário de apresentação de 0.</span><span class="sxs-lookup"><span data-stu-id="2dbcb-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2dbcb-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2dbcb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dbcb-123">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="2dbcb-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="2dbcb-124">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="2dbcb-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="2dbcb-125">**Usando comandos de script**</span><span class="sxs-lookup"><span data-stu-id="2dbcb-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




