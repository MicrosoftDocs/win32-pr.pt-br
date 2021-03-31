---
title: Formatos de entrada, configurações de entrada e extensões de unidade de dados
description: Formatos de entrada, configurações de entrada e extensões de unidade de dados
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- SDK do Windows Media Format, formatos de entrada e configurações
- SDK do Windows Media Format, extensões de unidade de dados
- SDK do Windows Media Format, sistemas de extensão de carga
- ASF (Advanced Systems Format), formatos de entrada e configurações
- ASF (formato de sistemas avançados), formatos de entrada e configurações
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- ASF (Advanced Systems Format), sistemas de extensão de carga
- ASF (formato de sistemas avançados), sistemas de extensão de carga
- extensões de unidade de dados, sobre
- sistemas de extensão de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916515"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="50809-114">Formatos de entrada, configurações de entrada e extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="50809-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="50809-115">O objeto gravador dá suporte a configurações de entrada, formatos de entrada e extensões de unidade de dados, todos os quais permitem controlar os recursos do gravador.</span><span class="sxs-lookup"><span data-stu-id="50809-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="50809-116">Nem sempre é óbvio quais métodos usar para controlar um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="50809-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="50809-117">Os formatos de entrada são formatos de mídia que descrevem as propriedades básicas da mídia que você passa para o gravador para codificação.</span><span class="sxs-lookup"><span data-stu-id="50809-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="50809-118">Por exemplo, o tamanho do quadro e o espaço de cores do vídeo de entrada são descritos pelo formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="50809-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="50809-119">As configurações de entrada são características dos dados de entrada além das noções básicas ou informações sobre transformações a serem executadas nos dados.</span><span class="sxs-lookup"><span data-stu-id="50809-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="50809-120">As configurações de vídeo entrelaçadas e as informações sobre um sistema de marca d' água são exemplos de configurações de entrada.</span><span class="sxs-lookup"><span data-stu-id="50809-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="50809-121">As extensões de unidade de dados, também chamadas de sistemas de extensão de carga, são valores anexados a amostras individuais na seção de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="50809-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="50809-122">Os códigos de tempo SMPTE e as informações de pixel não quadrado são exemplos de extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="50809-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50809-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50809-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50809-124">**Configurar extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="50809-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="50809-125">**Extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="50809-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="50809-126">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="50809-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="50809-127">**Enumeração de formato de entrada**</span><span class="sxs-lookup"><span data-stu-id="50809-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="50809-128">**Configurações de entrada**</span><span class="sxs-lookup"><span data-stu-id="50809-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="50809-129">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="50809-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




