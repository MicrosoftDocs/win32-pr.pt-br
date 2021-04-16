---
description: O campo comprimento em um TLV terceto identifica o número de bytes codificados no campo valor.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Comprimento codificado e bytes de valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758283"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="a3f49-103">Comprimento codificado e bytes de valor</span><span class="sxs-lookup"><span data-stu-id="a3f49-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="a3f49-104">O campo *comprimento* em um TLV terceto identifica o número de bytes codificados no campo *valor* .</span><span class="sxs-lookup"><span data-stu-id="a3f49-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="a3f49-105">O campo *valor* contém o conteúdo que está sendo enviado entre computadores.</span><span class="sxs-lookup"><span data-stu-id="a3f49-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="a3f49-106">Se o campo de *valor* contiver menos de 128 bytes, o campo *comprimento* exigirá apenas um byte.</span><span class="sxs-lookup"><span data-stu-id="a3f49-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="a3f49-107">O bit 7 do campo de *comprimento* é zero (0) e os bits restantes identificam o número de bytes de conteúdo que está sendo enviado.</span><span class="sxs-lookup"><span data-stu-id="a3f49-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="a3f49-108">Se o campo de *valor* contiver mais de 127 bytes, o bit 7 do campo de *comprimento* será um (1) e os bits restantes identificarão o número de bytes necessários para conter o comprimento.</span><span class="sxs-lookup"><span data-stu-id="a3f49-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="a3f49-109">Os exemplos são mostrados na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3f49-109">Examples are shown in the following illustration.</span></span>

![byte de comprimento de TLV der](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="a3f49-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3f49-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f49-112">Sintaxe de transferência de DER</span><span class="sxs-lookup"><span data-stu-id="a3f49-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="a3f49-113">Bytes de marca codificados</span><span class="sxs-lookup"><span data-stu-id="a3f49-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



