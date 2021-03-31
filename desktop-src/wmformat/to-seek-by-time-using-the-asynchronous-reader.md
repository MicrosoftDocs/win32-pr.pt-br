---
title: Para procurar por tempo usando o leitor assíncrono
description: Para procurar por tempo usando o leitor assíncrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- ASF (Advanced Systems Format), buscando por tempo
- ASF (formato de sistemas avançados), buscando por tempo
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, buscando por tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640162"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="abbea-108">Para procurar por tempo usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="abbea-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="abbea-109">Se você quiser buscar um tempo de apresentação específico em um arquivo ASF, o arquivo deverá ser configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="abbea-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="abbea-110">Você pode buscar apenas arquivos de áudio por padrão, mas os arquivos de vídeo precisam ser indexados antes de procurar.</span><span class="sxs-lookup"><span data-stu-id="abbea-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="abbea-111">Se você não tiver certeza de como um arquivo foi criado, poderá verificar o \_ atributo g wszWMSeekable no cabeçalho do arquivo chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="abbea-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="abbea-112">Para buscar dados em um arquivo ASF por hora de apresentação usando o leitor assíncrono, chame [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando a hora desejada e a duração da parte do arquivo que você deseja ler como *cnsStart* e *cnsDuration* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="abbea-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abbea-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abbea-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abbea-114">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="abbea-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="abbea-115">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="abbea-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="abbea-116">**Lendo metadados na reprodução**</span><span class="sxs-lookup"><span data-stu-id="abbea-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="abbea-117">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="abbea-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




