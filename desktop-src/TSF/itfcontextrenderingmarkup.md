---
title: Interface ITfContextRenderingMarkup
description: A interface ITfContextRenderingMarkup é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada usando IQueryInterface do objeto ITfContext. Essa interface ajuda o aplicativo a enumerar informações de renderização.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup, descrita
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823854"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="c1e7c-107">Interface ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="c1e7c-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="c1e7c-108">A interface **ITfContextRenderingMarkup** é implementada pelo Gerenciador do TSF e usada por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="c1e7c-109">Essa interface pode ser recuperada usando IQueryInterface do objeto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) .</span><span class="sxs-lookup"><span data-stu-id="c1e7c-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="c1e7c-110">Essa interface ajuda o aplicativo a enumerar informações de renderização.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="c1e7c-111">Métodos ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="c1e7c-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="c1e7c-112">Description</span><span class="sxs-lookup"><span data-stu-id="c1e7c-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c1e7c-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="c1e7c-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="c1e7c-114">Recupera um enumerador das marcações de renderização para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="c1e7c-115">FindNextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="c1e7c-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="c1e7c-116">Esta função não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-116">This function is not implemented.</span></span> <span data-ttu-id="c1e7c-117">Ele sempre retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="c1e7c-118">Membros</span><span class="sxs-lookup"><span data-stu-id="c1e7c-118">Members</span></span>

<span data-ttu-id="c1e7c-119">A interface **ITfContextRenderingMarkup** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e7c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1e7c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1e7c-121">Essa interface não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="c1e7c-122">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="c1e7c-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 