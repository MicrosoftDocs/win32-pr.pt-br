---
title: Marca LST
description: Marca LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498697"
---
# <a name="lst-tag"></a><span data-ttu-id="42c9a-103">Marca LST</span><span class="sxs-lookup"><span data-stu-id="42c9a-103">Lst Tag</span></span>

<span data-ttu-id="42c9a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42c9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="42c9a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="42c9a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42c9a-106">Repete a última instrução falada para o caractere.</span><span class="sxs-lookup"><span data-stu-id="42c9a-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="42c9a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="42c9a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="42c9a-108">\\**Ficheiro**</span><span class="sxs-lookup"><span data-stu-id="42c9a-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="42c9a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="42c9a-109">Remarks</span></span>

<span data-ttu-id="42c9a-110">Essa marca permite que um caractere repita sua última instrução falada.</span><span class="sxs-lookup"><span data-stu-id="42c9a-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="42c9a-111">Essa marca deve aparecer por si só no método [**Speak**](speak-method.md) ; nenhum outro texto ou parâmetro pode ser incluído.</span><span class="sxs-lookup"><span data-stu-id="42c9a-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="42c9a-112">Quando o texto falado é repetido, todas as outras marcas incluídas no texto original são repetidas, exceto os indicadores.</span><span class="sxs-lookup"><span data-stu-id="42c9a-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="42c9a-113">Outro. WAV e. Os arquivos LWV incluídos no texto também são repetidos.</span><span class="sxs-lookup"><span data-stu-id="42c9a-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




