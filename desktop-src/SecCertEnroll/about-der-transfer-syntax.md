---
description: A aplicação de uma regra de codificação às estruturas de dados descritas por uma sintaxe abstrata fornece uma sintaxe de transferência que governa como os bytes em um fluxo são organizados quando enviados entre computadores.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintaxe de transferência de DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556525"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="0f80f-103">Sintaxe de transferência de DER</span><span class="sxs-lookup"><span data-stu-id="0f80f-103">DER Transfer Syntax</span></span>

<span data-ttu-id="0f80f-104">A aplicação de uma regra de codificação às estruturas de dados descritas por uma sintaxe abstrata fornece uma sintaxe de transferência que governa como os bytes em um fluxo são organizados quando enviados entre computadores.</span><span class="sxs-lookup"><span data-stu-id="0f80f-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="0f80f-105">A sintaxe de transferência usada pelo Distinguished Encoding Rules sempre segue um formato *de marca, comprimento e valor* .</span><span class="sxs-lookup"><span data-stu-id="0f80f-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="0f80f-106">O formato geralmente é conhecido como um TLV terceto em que cada campo (T, L ou V) contém um ou mais bytes.</span><span class="sxs-lookup"><span data-stu-id="0f80f-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![tipo de der, comprimento e valor (TLV) terceto](images/der-tlv-basic.png)

<span data-ttu-id="0f80f-108">O campo de *marca* especifica o tipo da estrutura de dados que está sendo enviada, o campo *comprimento* especifica o número de bytes de conteúdo que está sendo transferido e o campo *valor* contém o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0f80f-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="0f80f-109">Observe que o campo de *valor* pode ser um terceto se ele contiver um tipo de dados construído, como mostrado pela ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f80f-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![recursão de terceto TLV de der](images/der-tlv-recursive.png)

<span data-ttu-id="0f80f-111">Consulte os tópicos a seguir para obter informações detalhadas sobre os componentes de um TLV terceto.</span><span class="sxs-lookup"><span data-stu-id="0f80f-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="0f80f-112">Bytes de marca codificados</span><span class="sxs-lookup"><span data-stu-id="0f80f-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="0f80f-113">Comprimento codificado e bytes de valor</span><span class="sxs-lookup"><span data-stu-id="0f80f-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="0f80f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f80f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f80f-115">Tipos construídos</span><span class="sxs-lookup"><span data-stu-id="0f80f-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="0f80f-116">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="0f80f-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



