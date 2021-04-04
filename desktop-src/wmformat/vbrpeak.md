---
title: VBRPeak
description: O atributo VBRPeak contém a taxa de bits momentânea mais alta em um fluxo codificado de taxa de bits variável (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Formato de mídia do Windows VBRPeak
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006636"
---
# <a name="vbrpeak"></a><span data-ttu-id="1b9de-104">VBRPeak</span><span class="sxs-lookup"><span data-stu-id="1b9de-104">VBRPeak</span></span>

<span data-ttu-id="1b9de-105">O atributo **VBRPeak** contém a taxa de bits momentânea mais alta em um fluxo codificado de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="1b9de-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1b9de-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="1b9de-106">Global Constant</span></span>

<span data-ttu-id="1b9de-107">g \_ wszVBRPeak</span><span class="sxs-lookup"><span data-stu-id="1b9de-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="1b9de-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1b9de-108">Data Type</span></span>

<span data-ttu-id="1b9de-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1b9de-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9de-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b9de-110">Remarks</span></span>

<span data-ttu-id="1b9de-111">Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="1b9de-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="1b9de-112">Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1b9de-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="1b9de-113">O gravador grava automaticamente um valor de **VBRPeak** para cada fluxo de VBR.</span><span class="sxs-lookup"><span data-stu-id="1b9de-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b9de-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b9de-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b9de-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="1b9de-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




