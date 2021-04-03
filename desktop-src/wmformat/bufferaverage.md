---
title: BufferAverage
description: O atributo BufferAverage contém o tamanho médio do buffer necessário para um fluxo de taxa de bits variável (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Formato de mídia do Windows BufferAverage
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084216"
---
# <a name="bufferaverage"></a><span data-ttu-id="ef53a-104">BufferAverage</span><span class="sxs-lookup"><span data-stu-id="ef53a-104">BufferAverage</span></span>

<span data-ttu-id="ef53a-105">O atributo **BufferAverage** contém o tamanho médio do buffer necessário para um fluxo de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="ef53a-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ef53a-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="ef53a-106">Global Constant</span></span>

<span data-ttu-id="ef53a-107">g \_ wszBufferAverage</span><span class="sxs-lookup"><span data-stu-id="ef53a-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="ef53a-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ef53a-108">Data Type</span></span>

<span data-ttu-id="ef53a-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ef53a-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="ef53a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef53a-110">Remarks</span></span>

<span data-ttu-id="ef53a-111">Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="ef53a-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="ef53a-112">Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ef53a-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="ef53a-113">O gravador grava automaticamente um valor de **BufferAverage** para cada fluxo de VBR.</span><span class="sxs-lookup"><span data-stu-id="ef53a-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef53a-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef53a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef53a-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="ef53a-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




