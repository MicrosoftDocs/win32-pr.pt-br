---
title: Entrada do registro FormatCode
description: Entrada do registro FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, entradas do registro FormatCode
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas FormatCode
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Entradas do registro FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104161789"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="73811-111">Entrada do registro FormatCode</span><span class="sxs-lookup"><span data-stu-id="73811-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="73811-112">Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="73811-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="73811-113">A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="73811-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="73811-114">Uma das entradas do registro que podem aparecer sob a subchave da extensão é a entrada **FormatCode** .</span><span class="sxs-lookup"><span data-stu-id="73811-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="73811-115">A entrada de registro **FormatCode** especifica o código de formato do MTP (protocolo de transporte de mídia) para arquivos que têm a extensão personalizada.</span><span class="sxs-lookup"><span data-stu-id="73811-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="73811-116">A entrada do registro **FormatCode** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="73811-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="73811-117">Nome</span><span class="sxs-lookup"><span data-stu-id="73811-117">Name</span></span>       | <span data-ttu-id="73811-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="73811-118">Type</span></span>           | <span data-ttu-id="73811-119">Valor</span><span class="sxs-lookup"><span data-stu-id="73811-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="73811-120">FormatCode</span><span class="sxs-lookup"><span data-stu-id="73811-120">FormatCode</span></span> | <span data-ttu-id="73811-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="73811-121">**REG\_DWORD**</span></span> | <span data-ttu-id="73811-122">Um inteiro positivo de 16 bits que identifica o formato do arquivo.</span><span class="sxs-lookup"><span data-stu-id="73811-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="73811-123">Quando o usuário tenta copiar um arquivo de mídia digital que tem uma extensão de nome de arquivo Personalizada para um dispositivo portátil, o Windows Media Player examina o registro para localizar um código de formato associado à extensão de nome de arquivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="73811-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="73811-124">Se o Windows Media Player encontrar um código de formato, ele usará MTP para determinar se o dispositivo dá suporte ao formato de arquivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="73811-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="73811-125">Se o dispositivo der suporte ao formato, o arquivo de mídia será copiado para o dispositivo sem ser transcodificado.</span><span class="sxs-lookup"><span data-stu-id="73811-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="73811-126">Um dispositivo que dá suporte a MTP pode fornecer ao Windows Media Player um conjunto de DeviceInfo, que contém, entre outras coisas, uma lista de códigos de formato com suporte pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73811-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="73811-127">Se você estiver no processo de desenvolvimento de um formato de arquivo personalizado, poderá solicitar um código de formato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73811-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="73811-128">Para obter informações sobre como solicitar um código de formato, consulte o Microsoft Media Transport Protocol Porting Kit, que está disponível no [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="73811-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73811-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73811-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73811-130">**Configurações do registro de extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="73811-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




