---
title: Estrutura de TF_RENDERINGMARKUP
description: A \_ estrutura de estrutura TF RENDERINGMARKUP contém um intervalo e as informações de atributo de exibição.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Estrutura de serviços de texto do TF_RENDERINGMARKUP Structure
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105813075"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="24fa9-104">Estrutura de RENDERINGMARKUP de TF \_</span><span class="sxs-lookup"><span data-stu-id="24fa9-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="24fa9-105">A estrutura de estrutura [**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contém um intervalo e as informações de atributo de exibição.</span><span class="sxs-lookup"><span data-stu-id="24fa9-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="24fa9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24fa9-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="24fa9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="24fa9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="24fa9-108">**pRange**</span><span class="sxs-lookup"><span data-stu-id="24fa9-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="24fa9-109">Um ponteiro para uma interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .</span><span class="sxs-lookup"><span data-stu-id="24fa9-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="24fa9-110">**tfDisplayAttr**</span><span class="sxs-lookup"><span data-stu-id="24fa9-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="24fa9-111">Exibir informações de atributo.</span><span class="sxs-lookup"><span data-stu-id="24fa9-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24fa9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="24fa9-112">Remarks</span></span>

<span data-ttu-id="24fa9-113">Essa estrutura não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="24fa9-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="24fa9-114">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="24fa9-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




