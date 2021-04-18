---
title: Método downloadcollection. startDownload
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método startDownload enfileira um download.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- método startDownload Windows Media Player
- método startDownload Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794488"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="5abd9-108">Método downloadcollection. startDownload</span><span class="sxs-lookup"><span data-stu-id="5abd9-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="5abd9-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5abd9-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5abd9-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5abd9-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5abd9-111">O método **startDownload** enfileira um download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abd9-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5abd9-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="5abd9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5abd9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5abd9-114">*sourceURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5abd9-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5abd9-115">**Cadeia de caracteres** que especifica a URL do download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="5abd9-116">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5abd9-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5abd9-117">**Cadeia de caracteres** que especifica o tipo de download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-117">**String** specifying the type of download.</span></span> <span data-ttu-id="5abd9-118">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="5abd9-118">Contains one of the following values.</span></span>



| <span data-ttu-id="5abd9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5abd9-119">Value</span></span>      | <span data-ttu-id="5abd9-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5abd9-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5abd9-121">background</span><span class="sxs-lookup"><span data-stu-id="5abd9-121">background</span></span> | <span data-ttu-id="5abd9-122">(Windows XP e posterior.) O download ocorre como um processo em segundo plano à medida que o tempo do processador se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="5abd9-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="5abd9-123">Os Estados de download persistem mesmo quando o Windows Media Player ou o Windows XP é desligado.</span><span class="sxs-lookup"><span data-stu-id="5abd9-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="5abd9-124">em tempo real</span><span class="sxs-lookup"><span data-stu-id="5abd9-124">real time</span></span>  | <span data-ttu-id="5abd9-125">(Todos os sistemas operacionais com suporte.) O download ocorre de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="5abd9-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="5abd9-126">Nenhum estado de download persiste entre sessões.</span><span class="sxs-lookup"><span data-stu-id="5abd9-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5abd9-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5abd9-127">Return value</span></span>

<span data-ttu-id="5abd9-128">Esse método retorna um objeto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="5abd9-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5abd9-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5abd9-129">Remarks</span></span>

<span data-ttu-id="5abd9-130">Quando um novo download é iniciado, o Gerenciador de download o adiciona como um item à coleção de download que iniciou o download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="5abd9-131">Somente os seguintes formatos de mídia digital podem ser baixados:</span><span class="sxs-lookup"><span data-stu-id="5abd9-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="5abd9-132">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="5abd9-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="5abd9-133">MP3</span><span class="sxs-lookup"><span data-stu-id="5abd9-133">MP3</span></span>
-   <span data-ttu-id="5abd9-134">Áudio do Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="5abd9-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="5abd9-135">Vídeo do Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="5abd9-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="5abd9-136">O parâmetro *sourceURL* não oferece suporte a cadeias de caracteres codificadas em Unicode.</span><span class="sxs-lookup"><span data-stu-id="5abd9-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="5abd9-137">Ele deve apontar para um conteúdo válido.</span><span class="sxs-lookup"><span data-stu-id="5abd9-137">It must point to valid content.</span></span> <span data-ttu-id="5abd9-138">Não há suporte para redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="5abd9-138">Redirects are not supported.</span></span>

<span data-ttu-id="5abd9-139">Ao usar o Windows XP, os arquivos de áudio são colocados automaticamente nas subpastas **minhas músicas** apropriadas com base nos valores de metadados de nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5abd9-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="5abd9-140">Os arquivos de vídeo são colocados em \\ minha música \\ baixar \\  \\ *tipo* de número aleatório, em que *número aleatório* é um valor aleatório gerado pelo Windows Media Player para cada usuário, e o *tipo* é "real time" ou "background", dependendo do tipo de download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="5abd9-141">Ao usar o Windows Media Player 9 Series com o Windows 98 e o Windows Millennium Edition (me), os arquivos de áudio e vídeo são colocados em \\ meu \\ \\ tipo de *número aleatório* de download de música \\ , em que o *número aleatório* é um valor aleatório gerado pelo Player para cada usuário, e o *tipo* é "real time" ou "background", dependendo do tipo de download.</span><span class="sxs-lookup"><span data-stu-id="5abd9-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="5abd9-142">Observe que os arquivos podem ser renomeados com base nos atributos de metadados contidos no arquivo e nas regras especificadas pelo usuário na caixa de diálogo **Opções** .</span><span class="sxs-lookup"><span data-stu-id="5abd9-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="5abd9-143">Os arquivos que não contêm metadados, como **álbum** ou **artista**, podem ser movidos para pastas rotuladas como artista desconhecido ou álbum desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5abd9-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="5abd9-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5abd9-144">Requirements</span></span>



| <span data-ttu-id="5abd9-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5abd9-145">Requirement</span></span> | <span data-ttu-id="5abd9-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5abd9-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5abd9-147">Versão</span><span class="sxs-lookup"><span data-stu-id="5abd9-147">Version</span></span><br/> | <span data-ttu-id="5abd9-148">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5abd9-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5abd9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5abd9-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="5abd9-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5abd9-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abd9-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="5abd9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abd9-152">**Objeto downloadcollection**</span><span class="sxs-lookup"><span data-stu-id="5abd9-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="5abd9-153">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="5abd9-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





