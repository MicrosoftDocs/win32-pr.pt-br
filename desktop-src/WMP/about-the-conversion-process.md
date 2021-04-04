---
title: Sobre o processo de conversão
description: Sobre o processo de conversão
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, processo de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007129"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="5fbb1-107">Sobre o processo de conversão</span><span class="sxs-lookup"><span data-stu-id="5fbb1-107">About the Conversion Process</span></span>

<span data-ttu-id="5fbb1-108">Depois que o Windows Media Player criar uma instância do plug-in de conversão, o processo continuará da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5fbb1-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="5fbb1-109">O Player chama [IWMPConvert:: converterfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span><span class="sxs-lookup"><span data-stu-id="5fbb1-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="5fbb1-110">O plug-in converte o arquivo fornecido no parâmetro *bstrInputFile* em um formato ASF.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="5fbb1-111">Se a conversão falhar por algum motivo, o plug-in retornará um código de falha apropriado e o processo será interrompido.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="5fbb1-112">Se a conversão for realizada com sucesso, o plug-in colocará o arquivo convertido na pasta fornecida no parâmetro *bstrDestinationFolder* e retornará o caminho totalmente qualificado para o arquivo convertido por meio do parâmetro *pbstrOutputFile* .</span><span class="sxs-lookup"><span data-stu-id="5fbb1-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="5fbb1-113">O plug-in retorna um código de êxito do **converterfile**.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="5fbb1-114">O Player copia o arquivo convertido em uma pasta na hierarquia de pastas de músicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="5fbb1-115">Exatamente para onde o Player copia o arquivo depende do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="5fbb1-116">Como parte desse processo, o player pode renomear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="5fbb1-117">O Player copia o arquivo original (não convertido) para uma pasta na hierarquia de pastas de músicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="5fbb1-118">Como parte desse processo, o player pode renomear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="5fbb1-119">Essa é a cópia do arquivo que o Player usa quando o usuário sincroniza o conteúdo do computador para um dispositivo que requer o formato de arquivo original.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="5fbb1-120">Esse arquivo é chamado de *arquivo de sombra*.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="5fbb1-121">O Player adiciona informações sobre o arquivo convertido à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="5fbb1-122">Isso inclui a definição do valor do atributo **ShadowFilePath** para o novo local onde o arquivo de sombra é salvo.</span><span class="sxs-lookup"><span data-stu-id="5fbb1-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="5fbb1-123">Se você precisar trabalhar com o arquivo convertido, poderá consultar a biblioteca para recuperar o conteúdo usando os atributos **ContentDistributor** e **WM/UniqueFileIdentifier** .</span><span class="sxs-lookup"><span data-stu-id="5fbb1-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="5fbb1-124">Se você precisar trabalhar com o arquivo de sombra, ainda deverá recuperar o objeto de **mídia** para o arquivo convertido e, em seguida, consultar o atributo **ShadowFilePath** .</span><span class="sxs-lookup"><span data-stu-id="5fbb1-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="5fbb1-125">Consulte [adicionando metadados a arquivos convertidos](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="5fbb1-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fbb1-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fbb1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fbb1-127">**Sobre plug-ins de conversão**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="5fbb1-128">**Adicionando metadados a arquivos convertidos**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="5fbb1-129">**Lendo valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="5fbb1-130">**Atributo ShadowFilePath**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="5fbb1-131">**Atributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="5fbb1-132">**Atributo WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="5fbb1-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




