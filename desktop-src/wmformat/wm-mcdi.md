---
title: WM/MCDI
description: O atributo WM/MCDI contém o identificador de CD de música. Este é um despejo binário do Sumário do CD que é usado para identificar exclusivamente o CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato de mídia do Windows do WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105785249"
---
# <a name="wmmcdi"></a><span data-ttu-id="967de-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="967de-105">WM/MCDI</span></span>

<span data-ttu-id="967de-106">O atributo **WM/MCDI** contém o identificador de CD de música.</span><span class="sxs-lookup"><span data-stu-id="967de-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="967de-107">Este é um despejo binário do Sumário do CD que é usado para identificar exclusivamente o CD.</span><span class="sxs-lookup"><span data-stu-id="967de-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="967de-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="967de-108">Global Constant</span></span>

<span data-ttu-id="967de-109">g \_ wszWMMCDI</span><span class="sxs-lookup"><span data-stu-id="967de-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="967de-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="967de-110">Data Type</span></span>

<span data-ttu-id="967de-111">**WMT \_ tipo \_ binário**</span><span class="sxs-lookup"><span data-stu-id="967de-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="967de-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="967de-112">Remarks</span></span>

<span data-ttu-id="967de-113">Esse atributo é compatível com o quadro ID3, MCDI.</span><span class="sxs-lookup"><span data-stu-id="967de-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="967de-114">A especificação ID3 para o quadro MCDI requer que apenas um desses quadros exista por arquivo e que exista um quadro TRCK válido.</span><span class="sxs-lookup"><span data-stu-id="967de-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="967de-115">O editor de metadados não executa nenhuma validação para essas regras.</span><span class="sxs-lookup"><span data-stu-id="967de-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="967de-116">Além disso, o tamanho do WM/MCDI não está limitado a 804 bytes, assim como o quadro ID3 MCDI.</span><span class="sxs-lookup"><span data-stu-id="967de-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="967de-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="967de-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967de-118">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="967de-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




