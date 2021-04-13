---
description: Este tópico descreve a estrutura de um arquivo ASF (Advanced Systems Format).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Estrutura de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501205"
---
# <a name="asf-file-structure"></a><span data-ttu-id="ec694-103">Estrutura de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="ec694-103">ASF File Structure</span></span>

<span data-ttu-id="ec694-104">Este tópico descreve a estrutura de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ec694-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="ec694-105">Para obter informações detalhadas sobre arquivos ASF, baixe a [especificação do ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="ec694-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="ec694-106">Você também pode usar a ferramenta do [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) para ver a estrutura de um arquivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="ec694-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="ec694-107">A unidade base da organização para arquivos ASF é chamada de *objeto*.</span><span class="sxs-lookup"><span data-stu-id="ec694-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="ec694-108">Um objeto de arquivo ASF contém os dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec694-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="ec694-109">Dados</span><span class="sxs-lookup"><span data-stu-id="ec694-109">Data</span></span>                                                        | <span data-ttu-id="ec694-110">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ec694-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="ec694-111">Um GUID que identifica o objeto.</span><span class="sxs-lookup"><span data-stu-id="ec694-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="ec694-112">128 bits</span><span class="sxs-lookup"><span data-stu-id="ec694-112">128 bits</span></span> |
| <span data-ttu-id="ec694-113">O tamanho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ec694-113">The size of the object.</span></span>                                     | <span data-ttu-id="ec694-114">64 bits.</span><span class="sxs-lookup"><span data-stu-id="ec694-114">64-bits.</span></span> |
| <span data-ttu-id="ec694-115">Dados do objeto.</span><span class="sxs-lookup"><span data-stu-id="ec694-115">Object data.</span></span> <span data-ttu-id="ec694-116">Os dados do objeto podem conter outros objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="ec694-117">Varia.</span><span class="sxs-lookup"><span data-stu-id="ec694-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="ec694-118">Um objeto de arquivo ASF é simplesmente uma parte dos dados.</span><span class="sxs-lookup"><span data-stu-id="ec694-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="ec694-119">Não é um objeto no sentido de programação do computador.</span><span class="sxs-lookup"><span data-stu-id="ec694-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="ec694-120">Um arquivo ASF contém três tipos de objetos de arquivo de nível superior.</span><span class="sxs-lookup"><span data-stu-id="ec694-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="ec694-121">Objeto de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="ec694-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="ec694-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec694-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec694-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objeto de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec694-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="ec694-124">Contém informações sobre o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="ec694-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objeto de dados</span><span class="sxs-lookup"><span data-stu-id="ec694-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="ec694-126">Contém pacotes de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="ec694-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="ec694-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objeto (s) de índice</span><span class="sxs-lookup"><span data-stu-id="ec694-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="ec694-128">Contém um ou mais índices.</span><span class="sxs-lookup"><span data-stu-id="ec694-128">Contains one or more indexes.</span></span> <span data-ttu-id="ec694-129">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="ec694-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="ec694-130">O diagrama a seguir mostra a estrutura do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-130">The following diagram shows the ASF file structure.</span></span>

![diagrama mostrando a estrutura do arquivo ASF, incluindo itens dentro do cabeçalho, dos dados e do índice](images/asf-components04.png)

<span data-ttu-id="ec694-132">Este diagrama não é desenhado para escala; Normalmente, o objeto de dados compreende a maior parte do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ec694-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="ec694-133">Objeto de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec694-133">Header Object</span></span>

<span data-ttu-id="ec694-134">O objeto de cabeçalho é obrigatório e aparece no início de cada arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="ec694-135">Ele contém atributos de arquivo globais e informações sobre os fluxos no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="ec694-136">Essas informações são usadas para interpretar e reproduzir os dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ec694-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="ec694-137">O objeto de cabeçalho contém vários subobjetos madatory:</span><span class="sxs-lookup"><span data-stu-id="ec694-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="ec694-138">O objeto de propriedades de arquivo descreve os atributos globais do arquivo, como o tamanho do arquivo, a duração da reprodução, o número de pacotes de dados, o tamanho mínimo e máximo do pacote e a taxa de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="ec694-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="ec694-139">O objeto de extensão de cabeçalho permite que a funcionalidade adicional seja adicionada a um arquivo ASF, mantendo a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="ec694-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="ec694-140">O objeto de propriedades de fluxo descreve um fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ec694-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="ec694-141">Um arquivo ASF deve conter pelo menos um fluxo e, portanto, pelo menos um objeto de propriedades de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ec694-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="ec694-142">O objeto de cabeçalho pode conter informações adicionais opcionais, incluindo metadados sobre o arquivo (como título e autor), uma lista dos codecs usados para codificar o arquivo e informações de proteção de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ec694-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="ec694-143">Objeto de dados</span><span class="sxs-lookup"><span data-stu-id="ec694-143">Data Object</span></span>

<span data-ttu-id="ec694-144">O objeto de dados ASF contém todos os dados de mídia para o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="ec694-145">Esse objeto é obrigatório e deve seguir o objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="ec694-146">O objeto de dados é dividido em *pacotes* de dados.</span><span class="sxs-lookup"><span data-stu-id="ec694-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="ec694-147">Cada pacote contém dados para um ou vários fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ec694-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="ec694-148">Um pacote de dados contém um cabeçalho de pacote de dados que fornece informações de análise de pacote, seguidos pelos dados de carga dos dados de mídia digital reais.</span><span class="sxs-lookup"><span data-stu-id="ec694-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="ec694-149">Todos os pacotes de dados têm um tempo de apresentação associado a ele e são organizados na ordem recebida.</span><span class="sxs-lookup"><span data-stu-id="ec694-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="ec694-150">As informações sobre o conteúdo do objeto de dados, como o tamanho do pacote e a contagem de pacotes, são armazenadas no objeto de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ec694-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="ec694-151">Objeto de índice</span><span class="sxs-lookup"><span data-stu-id="ec694-151">Index Object</span></span>

<span data-ttu-id="ec694-152">O objeto de índice é opcional e é o último objeto no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="ec694-153">Um arquivo ASF pode conter mais de um objeto de índice.</span><span class="sxs-lookup"><span data-stu-id="ec694-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="ec694-154">O objeto Index fornece acesso aleatório baseado em tempo ao objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="ec694-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="ec694-155">Um objeto de índice simples é outro tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="ec694-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec694-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec694-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec694-157">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec694-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




