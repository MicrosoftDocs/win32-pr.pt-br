---
description: Solicitação de informações do arquivo de origem de uma pilha de chamadas.
MS-HAID: vspixengine.ISourceFileInfoRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ISourceFileInfoRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 69C50343-32F0-46AE-B724-36EBD8AA8DF9
api_name:
- ISourceFileInfoRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0aca47f2aa8a03db787cffcf911a30559aeeb82
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456695"
---
# <a name="span-idvspixengineisourcefileinforequestspanisourcefileinforequest-interface"></a><span data-ttu-id="f219c-103"><span id="vspixengine.isourcefileinforequest"></span>Interface ISourceFileInfoRequest</span><span class="sxs-lookup"><span data-stu-id="f219c-103"><span id="vspixengine.isourcefileinforequest"></span>ISourceFileInfoRequest interface</span></span>

<span data-ttu-id="f219c-104">Solicitação de informações do arquivo de origem de uma pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="f219c-104">Request for source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="f219c-105">Membros</span><span class="sxs-lookup"><span data-stu-id="f219c-105">Members</span></span>

<span data-ttu-id="f219c-106">A interface **ISourceFileInfoRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f219c-106">The **ISourceFileInfoRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f219c-107">**ISourceFileInfoRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f219c-107">**ISourceFileInfoRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="f219c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f219c-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f219c-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="f219c-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f219c-110">A interface **ISourceFileInfoRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f219c-110">The **ISourceFileInfoRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f219c-111">Método</span><span class="sxs-lookup"><span data-stu-id="f219c-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f219c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f219c-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f219c-113"><a href="/windows/desktop/direct3dtools/isourcefileinforequest-requestasync-eventid-isourcefileinfocallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="f219c-113"><a href="/windows/desktop/direct3dtools/isourcefileinforequest-requestasync-eventid-isourcefileinfocallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f219c-114">Uma solicitação assíncrona para obter os arquivos de origem associados à pilha de chamadas de um evento.</span><span class="sxs-lookup"><span data-stu-id="f219c-114">An asynchronous request to get the source files associated with the callstack of an event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f219c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f219c-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f219c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f219c-116">Header</span></span></p></td><td><span data-ttu-id="f219c-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f219c-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
