---
description: Requisitos para recursos
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisitos para recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170677"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="74d58-103">Requisitos para recursos</span><span class="sxs-lookup"><span data-stu-id="74d58-103">Requirements for Resources</span></span>

<span data-ttu-id="74d58-104">Os dispositivos portáteis do Windows definem as seguintes categorias de recursos como valores de **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="74d58-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="74d58-105">Esses valores são usados para descrever recursos individuais em um objeto.</span><span class="sxs-lookup"><span data-stu-id="74d58-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="74d58-106">O membro *pid* da chave de propriedade pode ser diferente para descrever recursos diferentes do mesmo tipo para todos os tipos, exceto o **\_ \_ padrão de recursos WPD**, que pode descrever apenas um recurso.</span><span class="sxs-lookup"><span data-stu-id="74d58-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="74d58-107">A página descrição vinculada para cada tipo de recurso lista os atributos suportados por esse recurso.</span><span class="sxs-lookup"><span data-stu-id="74d58-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="74d58-108">PROPERTYKEY do recurso</span><span class="sxs-lookup"><span data-stu-id="74d58-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="74d58-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="74d58-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74d58-110">**\_padrão de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="74d58-111">Especifica o arquivo inteiro por trás do objeto.</span><span class="sxs-lookup"><span data-stu-id="74d58-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="74d58-112">Esse é o único recurso necessário para qualquer objeto com um recurso.</span><span class="sxs-lookup"><span data-stu-id="74d58-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="74d58-113">**\_arte do \_ álbum de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="74d58-114">Especifica uma imagem que representa a arte-final do álbum do objeto.</span><span class="sxs-lookup"><span data-stu-id="74d58-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="74d58-115">**\_clipe de \_ áudio de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="74d58-116">Especifica um clipe de áudio para o objeto.</span><span class="sxs-lookup"><span data-stu-id="74d58-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="74d58-117">**\_foto de \_ contato de recursos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="74d58-118">Especifica uma imagem que representa uma foto do indivíduo referenciado no objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="74d58-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="74d58-119">**recurso de WPD \_ \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="74d58-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="74d58-120">Um recurso genérico de tipo de dados indefinido.</span><span class="sxs-lookup"><span data-stu-id="74d58-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="74d58-121">Isso deve ser tratado como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="74d58-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="74d58-122">**\_ícone de recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="74d58-123">Um ícone.</span><span class="sxs-lookup"><span data-stu-id="74d58-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="74d58-124">**\_miniatura do recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74d58-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="74d58-125">Uma imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="74d58-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="74d58-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74d58-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74d58-127">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="74d58-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



