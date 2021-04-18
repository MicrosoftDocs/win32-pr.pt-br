---
description: Decoder-Specific entradas do registro
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785946"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="59e5c-103">Decoder-Specific entradas do registro</span><span class="sxs-lookup"><span data-stu-id="59e5c-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="59e5c-104">Além das entradas de Registro necessárias para todos os codificadores e decodificadores, as seguintes entradas de registro são necessárias especificamente para decodificadores.</span><span class="sxs-lookup"><span data-stu-id="59e5c-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="59e5c-105">Essas entradas registram seu decodificador na categoria de decodificadores do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="59e5c-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="59e5c-106">O primeiro GUID nessas entradas é o identificador de categoria (CATID) para [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="59e5c-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="59e5c-107">Como observado na seção [descoberta e arbitragem](-wic-howwicworks.md) de como funciona o Windows Imaging Component, o mecanismo que permite que um decodificador apropriado para uma imagem específica seja descoberto em tempo de execução é baseado na correspondência de um padrão de identificação inserido no arquivo de imagem com um padrão especificado na entrada de registro do decodificador.</span><span class="sxs-lookup"><span data-stu-id="59e5c-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="59e5c-108">Para habilitar a descoberta em tempo de execução de decodificadores, você deve registrar o padrão de identificação exclusivo para o formato de imagem da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="59e5c-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="59e5c-109">Todas essas entradas de registro são necessárias, exceto a entrada **EndOfStream** , que é opcional, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="59e5c-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="59e5c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="59e5c-110">Value</span></span>       | <span data-ttu-id="59e5c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="59e5c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e5c-112">Posição</span><span class="sxs-lookup"><span data-stu-id="59e5c-112">Position</span></span>    | <span data-ttu-id="59e5c-113">O deslocamento no arquivo onde o padrão pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="59e5c-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="59e5c-114">Comprimento</span><span class="sxs-lookup"><span data-stu-id="59e5c-114">Length</span></span>      | <span data-ttu-id="59e5c-115">O comprimento do padrão.</span><span class="sxs-lookup"><span data-stu-id="59e5c-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="59e5c-116">Padrão</span><span class="sxs-lookup"><span data-stu-id="59e5c-116">Pattern</span></span>     | <span data-ttu-id="59e5c-117">Os bits reais que compõem o padrão.</span><span class="sxs-lookup"><span data-stu-id="59e5c-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="59e5c-118">Esses são os bits que correspondem ao padrão de identificação em um arquivo de imagem durante a descoberta.</span><span class="sxs-lookup"><span data-stu-id="59e5c-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="59e5c-119">Mask</span><span class="sxs-lookup"><span data-stu-id="59e5c-119">Mask</span></span>        | <span data-ttu-id="59e5c-120">Permite valores curinga em padrões.</span><span class="sxs-lookup"><span data-stu-id="59e5c-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="59e5c-121">A máscara é aplicada pela execução de uma operação AND lógica no padrão e na máscara.</span><span class="sxs-lookup"><span data-stu-id="59e5c-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="59e5c-122">Qualquer bit no padrão que corresponda a um bit na máscara com um valor de 0 é ignorado.</span><span class="sxs-lookup"><span data-stu-id="59e5c-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="59e5c-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="59e5c-123">EndOfStream</span></span> | <span data-ttu-id="59e5c-124">O deslocamento do padrão de identificação deve ser calculado a partir do final do fluxo, em vez do início.</span><span class="sxs-lookup"><span data-stu-id="59e5c-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="59e5c-125">Alguns formatos de imagem colocam o padrão de identificação no final do arquivo ou próximo dele.</span><span class="sxs-lookup"><span data-stu-id="59e5c-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="59e5c-126">Como o padrão é buscar desde o início, a menos que o padrão esteja próximo do final do arquivo, você pode omitir essa entrada.</span><span class="sxs-lookup"><span data-stu-id="59e5c-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="59e5c-127">Um codec pode dar suporte a mais de um padrão de identificação.</span><span class="sxs-lookup"><span data-stu-id="59e5c-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="59e5c-128">Nesse caso, você repetiria todas as chaves em padrões de **\_ classe HKEY \_ \\ \\ {Decoder CLSID} \\ Patterns** e usará a chave numérica (0 no exemplo) para distinguir entre os diferentes padrões.</span><span class="sxs-lookup"><span data-stu-id="59e5c-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="59e5c-129">Você deve incluir cada um dos quatro valores na chave para cada padrão.</span><span class="sxs-lookup"><span data-stu-id="59e5c-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="59e5c-130">Registrando um formato de contêiner com leitores de metadados</span><span class="sxs-lookup"><span data-stu-id="59e5c-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="59e5c-131">Se você criar um novo formato de contêiner para o codec, também deverá criar entradas de registro para dar suporte à descoberta de leitores de metadados para os blocos de metadados em suas imagens, assim como você fez para os gravadores de metadados.</span><span class="sxs-lookup"><span data-stu-id="59e5c-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="59e5c-132">As entradas a seguir precisam ser criadas no identificador de classe (CLSID) do leitor de metadados para cada formato de metadados com suporte no formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="59e5c-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="59e5c-133">(Observe que, se o seu codec usar um contêiner TIFF, então essa informação já estará no registro.)</span><span class="sxs-lookup"><span data-stu-id="59e5c-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="59e5c-134">Como as entradas para leitores de metadados também são usadas para descoberta, elas são muito semelhantes às entradas para decodificadores.</span><span class="sxs-lookup"><span data-stu-id="59e5c-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="59e5c-135">Essas entradas são usadas pela fábrica de componentes para localizar os leitores de metadados com suporte no seu contêiner e para selecionar o apropriado, quando sua implementação de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) solicitar um leitor de metadados.</span><span class="sxs-lookup"><span data-stu-id="59e5c-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="59e5c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="59e5c-136">Value</span></span>      | <span data-ttu-id="59e5c-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="59e5c-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e5c-138">Posição</span><span class="sxs-lookup"><span data-stu-id="59e5c-138">Position</span></span>   | <span data-ttu-id="59e5c-139">O deslocamento no contêiner do bloco de metadados onde o cabeçalho de metadados pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="59e5c-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="59e5c-140">Para blocos de metadados de nível superior, esse é o deslocamento no fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="59e5c-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="59e5c-141">Para blocos de metadados aninhados em outros blocos de metadados, é o deslocamento relativo ao bloco de metadados recipiente.</span><span class="sxs-lookup"><span data-stu-id="59e5c-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="59e5c-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="59e5c-142">Pattern</span></span>    | <span data-ttu-id="59e5c-143">Os bits reais que compõem o padrão.</span><span class="sxs-lookup"><span data-stu-id="59e5c-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="59e5c-144">Esses são os bits que correspondem ao padrão de identificação em um arquivo de imagem durante a descoberta.</span><span class="sxs-lookup"><span data-stu-id="59e5c-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="59e5c-145">Mask</span><span class="sxs-lookup"><span data-stu-id="59e5c-145">Mask</span></span>       | <span data-ttu-id="59e5c-146">O cabeçalho de metadados geralmente é definido pelo manipulador de metadados.</span><span class="sxs-lookup"><span data-stu-id="59e5c-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="59e5c-147">Você deve usar o cabeçalho de metadados padrão para cada leitor, a menos que, por algum motivo, o padrão deva ter um formato diferente em seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="59e5c-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="59e5c-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="59e5c-148">DataOffset</span></span> | <span data-ttu-id="59e5c-149">O deslocamento do início do cabeçalho de metadados no qual os dados reais começam.</span><span class="sxs-lookup"><span data-stu-id="59e5c-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="59e5c-150">Nos casos em que os metadados não estão localizados em um deslocamento específico do cabeçalho, essa entrada pode ser omitida.</span><span class="sxs-lookup"><span data-stu-id="59e5c-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="59e5c-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59e5c-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="59e5c-152">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="59e5c-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59e5c-153">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="59e5c-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="59e5c-154">Integração com a Galeria de fotos do Windows e o Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="59e5c-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="59e5c-155">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="59e5c-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="59e5c-156">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="59e5c-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



