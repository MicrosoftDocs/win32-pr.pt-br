---
description: A interface IMediaLocator fornece métodos para validar nomes de arquivo nos serviços de edição do DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interface IMediaLocator (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759074"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="647b7-103">Interface IMediaLocator</span><span class="sxs-lookup"><span data-stu-id="647b7-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="647b7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="647b7-104">\[Deprecated.</span></span> <span data-ttu-id="647b7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="647b7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="647b7-106">A `IMediaLocator` interface fornece métodos para validar nomes de arquivo nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="647b7-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="647b7-107">Use essa interface para garantir que um determinado nome de arquivo e caminho correspondam a um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="647b7-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="647b7-108">Essa interface também fornece uma maneira de Pesquisar o arquivo em outros locais e exibir uma caixa de diálogo **aberta** para que o usuário possa localizar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="647b7-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="647b7-109">O localizador de mídia implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="647b7-109">The media locator implements this interface.</span></span> <span data-ttu-id="647b7-110">A linha do tempo e o mecanismo de processamento também dão suporte à validação de nome de arquivo por meio dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="647b7-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="647b7-111">[**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valida e atualiza os nomes de arquivo na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="647b7-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="647b7-112">[**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): especifica como o mecanismo de renderização valida nomes de arquivo no momento da renderização.</span><span class="sxs-lookup"><span data-stu-id="647b7-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="647b7-113">Normalmente, um aplicativo DES chamará esses métodos em vez de criar diretamente uma instância do localizador de mídia.</span><span class="sxs-lookup"><span data-stu-id="647b7-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="647b7-114">Para obter mais informações, consulte [usando o localizador de mídia](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="647b7-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="647b7-115">Membros</span><span class="sxs-lookup"><span data-stu-id="647b7-115">Members</span></span>

<span data-ttu-id="647b7-116">A interface **IMediaLocator** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="647b7-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="647b7-117">**IMediaLocator** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="647b7-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="647b7-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="647b7-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="647b7-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="647b7-119">Methods</span></span>

<span data-ttu-id="647b7-120">A interface **IMediaLocator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="647b7-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="647b7-121">Método</span><span class="sxs-lookup"><span data-stu-id="647b7-121">Method</span></span>                                                     | <span data-ttu-id="647b7-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="647b7-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="647b7-123">**AddFoundLocation**</span><span class="sxs-lookup"><span data-stu-id="647b7-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="647b7-124">Adiciona um diretório ao cache de diretório.</span><span class="sxs-lookup"><span data-stu-id="647b7-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="647b7-125">**FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="647b7-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="647b7-126">Procura um arquivo e, se for bem-sucedido, recupera o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="647b7-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="647b7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="647b7-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="647b7-128">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="647b7-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="647b7-129">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="647b7-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="647b7-130">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="647b7-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="647b7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647b7-131">Requirements</span></span>



| <span data-ttu-id="647b7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="647b7-132">Requirement</span></span> | <span data-ttu-id="647b7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="647b7-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="647b7-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="647b7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="647b7-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="647b7-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="647b7-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="647b7-136">Library</span></span><br/> | <dl> <span data-ttu-id="647b7-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="647b7-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
