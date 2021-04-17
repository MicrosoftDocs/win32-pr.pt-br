---
title: Registrando plug-ins de conversão
description: Registrando plug-ins de conversão
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, plug-ins de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, registrando
- registro, plug-ins de conversão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779986"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="77967-108">Registrando plug-ins de conversão</span><span class="sxs-lookup"><span data-stu-id="77967-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="77967-109">Formatos de terceiros devem ser registrados antes que o Windows Media Player possa criar uma instância e usar o plug-in de conversão.</span><span class="sxs-lookup"><span data-stu-id="77967-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="77967-110">Para registrar seu arquivo para conversão, você deve registrar a extensão de nome de arquivo associada ao seu formato.</span><span class="sxs-lookup"><span data-stu-id="77967-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="77967-111">A lista de extensões de nome de arquivo registrada é mantida como um conjunto de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="77967-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="77967-112">Para obter detalhes sobre como registrar formatos de terceiros, consulte [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="77967-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="77967-113">A tabela a seguir lista as configurações de valor do registro para registrar um formato de terceiros para conversão usando um plug-in de conversão.</span><span class="sxs-lookup"><span data-stu-id="77967-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="77967-114">Valor</span><span class="sxs-lookup"><span data-stu-id="77967-114">Value</span></span>                  | <span data-ttu-id="77967-115">Configuração</span><span class="sxs-lookup"><span data-stu-id="77967-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="77967-116">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="77967-116">**Runtime**</span></span>            | <span data-ttu-id="77967-117">13</span><span class="sxs-lookup"><span data-stu-id="77967-117">13</span></span>                                                          |
| <span data-ttu-id="77967-118">**Permissões**</span><span class="sxs-lookup"><span data-stu-id="77967-118">**Permissions**</span></span>        | <span data-ttu-id="77967-119">8 (permissão para a biblioteca).</span><span class="sxs-lookup"><span data-stu-id="77967-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="77967-120">**ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="77967-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="77967-121">A ID de classe do plug-in de conversão, no formato de registro.</span><span class="sxs-lookup"><span data-stu-id="77967-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="77967-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77967-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77967-123">**Referência de programação de plug-ins de conversão**</span><span class="sxs-lookup"><span data-stu-id="77967-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




