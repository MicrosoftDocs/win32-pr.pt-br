---
title: Objeto de imagem padrão
description: Objeto de imagem padrão
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917707"
---
# <a name="standard-picture-object"></a><span data-ttu-id="bf617-103">Objeto de imagem padrão</span><span class="sxs-lookup"><span data-stu-id="bf617-103">Standard Picture Object</span></span>

<span data-ttu-id="bf617-104">O objeto de imagem padrão fornece uma abstração neutra de idioma para imagens GDI: bitmaps, ícones, metaarquivos e metaarquivos aprimorados.</span><span class="sxs-lookup"><span data-stu-id="bf617-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="bf617-105">Assim como acontece com o objeto de fonte padrão, o sistema fornece uma implementação padrão desse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf617-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="bf617-106">Suas interfaces primárias são [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), a última deriva de **IDispatch** para fornecer acesso às propriedades da imagem por meio da automação OLE.</span><span class="sxs-lookup"><span data-stu-id="bf617-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="bf617-107">Um objeto de imagem é criado com [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="bf617-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="bf617-108">O objeto Picture também dá suporte à interface de saída [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que um cliente possa determinar quando as propriedades da imagem são alteradas.</span><span class="sxs-lookup"><span data-stu-id="bf617-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="bf617-109">Da mesma forma, o objeto Picture também dá suporte a [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e a um ponto de conexão para **IPropertyNotifySink**.</span><span class="sxs-lookup"><span data-stu-id="bf617-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="bf617-110">O objeto Picture também dá suporte a [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , de modo que ele pode salvar e carregar a si mesmo de uma instância de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="bf617-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="bf617-111">Um objeto que usa um objeto de imagem internamente normalmente salva e carrega a imagem como parte da própria manipulação de persistência do objeto.</span><span class="sxs-lookup"><span data-stu-id="bf617-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="bf617-112">A função [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifica a criação de um objeto de imagem com base no conteúdo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="bf617-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf617-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf617-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf617-114">Propriedades de controle</span><span class="sxs-lookup"><span data-stu-id="bf617-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 