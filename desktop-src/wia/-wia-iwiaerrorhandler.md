---
description: A interface IWiaErrorHandler fornece métodos para lidar com erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para os bits de visualização ou final.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interface IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090802"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="2097a-103">Interface IWiaErrorHandler</span><span class="sxs-lookup"><span data-stu-id="2097a-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="2097a-104">A interface **IWiaErrorHandler** fornece métodos para lidar com erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para os bits de visualização ou final.</span><span class="sxs-lookup"><span data-stu-id="2097a-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="2097a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="2097a-105">Members</span></span>

<span data-ttu-id="2097a-106">A interface **IWiaErrorHandler** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2097a-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2097a-107">**IWiaErrorHandler** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2097a-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="2097a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2097a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2097a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2097a-109">Methods</span></span>

<span data-ttu-id="2097a-110">A interface **IWiaErrorHandler** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2097a-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="2097a-111">Método</span><span class="sxs-lookup"><span data-stu-id="2097a-111">Method</span></span>                                                                     | <span data-ttu-id="2097a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2097a-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2097a-113">**GetStatusDescription**</span><span class="sxs-lookup"><span data-stu-id="2097a-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="2097a-114">Retorna uma cadeia de caracteres que descreve o código de status.</span><span class="sxs-lookup"><span data-stu-id="2097a-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="2097a-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="2097a-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="2097a-116">Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2097a-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2097a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2097a-117">Remarks</span></span>

<span data-ttu-id="2097a-118">O objeto de retorno de chamada do aplicativo pode implementar **IWiaErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="2097a-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="2097a-119">Esta interface não foi projetada para lidar com erros encontrados fora das transferências de dados de imagem, por exemplo, erros ao obter ou definir propriedades de dispositivo ou retornos de chamada não retornados em um driver.</span><span class="sxs-lookup"><span data-stu-id="2097a-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="2097a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2097a-120">Requirements</span></span>



| <span data-ttu-id="2097a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2097a-121">Requirement</span></span> | <span data-ttu-id="2097a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2097a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2097a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2097a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2097a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2097a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2097a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2097a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2097a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2097a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2097a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2097a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2097a-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2097a-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="2097a-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="2097a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2097a-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2097a-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="2097a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2097a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2097a-132"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2097a-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
