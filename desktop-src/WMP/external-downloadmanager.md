---
title: Externo. DownloadManager
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade DownloadManager recupera o objeto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Externo. DownloadManager Windows Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779999"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="67c5b-106">Externo. DownloadManager</span><span class="sxs-lookup"><span data-stu-id="67c5b-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="67c5b-107">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="67c5b-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="67c5b-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="67c5b-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="67c5b-109">A propriedade **DownloadManager** recupera o objeto **DownloadManager** .</span><span class="sxs-lookup"><span data-stu-id="67c5b-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="67c5b-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="67c5b-110">Possible Values</span></span>

<span data-ttu-id="67c5b-111">Esta propriedade é um objeto **DownloadManager** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67c5b-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c5b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="67c5b-112">Remarks</span></span>

<span data-ttu-id="67c5b-113">No Windows Media Player 10 ou posterior, a propriedade e o objeto **DownloadManager** são acessíveis somente de painéis de tarefas do serviço de loja online.</span><span class="sxs-lookup"><span data-stu-id="67c5b-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="67c5b-114">Você não pode usar o **DownloadManager** de outros recursos em que o objeto **externo** está disponível, como HtmlView, exibição do centro de informações e informações do álbum.</span><span class="sxs-lookup"><span data-stu-id="67c5b-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c5b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c5b-115">Requirements</span></span>



| <span data-ttu-id="67c5b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c5b-116">Requirement</span></span> | <span data-ttu-id="67c5b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="67c5b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67c5b-118">Versão</span><span class="sxs-lookup"><span data-stu-id="67c5b-118">Version</span></span><br/> | <span data-ttu-id="67c5b-119">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="67c5b-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="67c5b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="67c5b-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="67c5b-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c5b-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c5b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="67c5b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c5b-123">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="67c5b-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





