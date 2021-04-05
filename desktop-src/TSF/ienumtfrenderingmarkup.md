---
title: Interface IEnumTfRenderingMarkup
description: A interface IEnumTfRenderingMarkup é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada por ITfContextRenderingMarkup GetRenderingMarkup e enumera as informações de marcação de renderização.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, descrita
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007959"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="1197f-106">Interface IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="1197f-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="1197f-107">A interface **IEnumTfRenderingMarkup** é implementada pelo Gerenciador do TSF e usada por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1197f-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="1197f-108">Essa interface pode ser recuperada por [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) e enumera as informações de marcação de renderização.</span><span class="sxs-lookup"><span data-stu-id="1197f-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="1197f-109">Métodos IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="1197f-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="1197f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1197f-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1197f-111">8i</span><span class="sxs-lookup"><span data-stu-id="1197f-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="1197f-112">O método **IEnumTfRenderingMarkup:: clone** cria uma cópia do objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="1197f-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="1197f-113">Próximo</span><span class="sxs-lookup"><span data-stu-id="1197f-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="1197f-114">O método **IEnumTfRenderingMarkup:: Next** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="1197f-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="1197f-115">Redefinir</span><span class="sxs-lookup"><span data-stu-id="1197f-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="1197f-116">O método **IEnumTfRenderingMarkup:: Reset** redefine o objeto enumerador movendo a posição atual para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="1197f-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="1197f-117">Skip</span><span class="sxs-lookup"><span data-stu-id="1197f-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="1197f-118">O método **IEnumTfRenderingMarkup:: Skip** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="1197f-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="1197f-119">Membros</span><span class="sxs-lookup"><span data-stu-id="1197f-119">Members</span></span>

<span data-ttu-id="1197f-120">A interface **IEnumTfRenderingMarkup** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="1197f-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1197f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1197f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1197f-122">Essa interface não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="1197f-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="1197f-123">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="1197f-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 