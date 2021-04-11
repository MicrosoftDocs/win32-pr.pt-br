---
title: Para editar metadados com o gravador
description: Para editar metadados com o gravador
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- SDK do Windows Media Format, editando metadados com o gravador
- SDK do Windows Media Format, edição de metadados
- ASF (Advanced Systems Format), editando metadados com o gravador
- ASF (formato de sistemas avançados), editando metadados com o gravador
- ASF (Advanced Systems Format), edição de metadados
- ASF (formato de sistemas avançados), edição de metadados
- metadados, edição com o gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365755"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="c20d9-110">Para editar metadados com o gravador</span><span class="sxs-lookup"><span data-stu-id="c20d9-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="c20d9-111">Você pode acessar o, diretamente do gravador, os metadados que vão para o cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c20d9-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="c20d9-112">Chame o método **QueryInterface** de qualquer interface no objeto do gravador para obter um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="c20d9-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="c20d9-113">Depois de ter um ponteiro para a interface apropriada, você poderá manipular os metadados da mesma forma que faria se tivesse carregado o arquivo no objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="c20d9-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="c20d9-114">Para obter mais informações sobre como editar metadados, consulte [trabalhando com metadados](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="c20d9-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="c20d9-115">Você deve fazer todas as alterações nos metadados antes de chamar [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="c20d9-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="c20d9-116">Se você definir metadados para um arquivo, gravar o arquivo e, em seguida, se preparar para gravar um novo arquivo sem liberar o gravador, alguns metadados que foram definidos para o primeiro arquivo permanecerão definidos e serão incluídos nos arquivos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c20d9-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="c20d9-117">Ao gravar vários arquivos com a mesma instância do objeto Writer, você tem duas opções: verificar todos os metadados antes de gravar cada arquivo ou apenas gravar os metadados do gravador que se aplicam a todos os arquivos que você está gravando.</span><span class="sxs-lookup"><span data-stu-id="c20d9-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c20d9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c20d9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c20d9-119">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="c20d9-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




