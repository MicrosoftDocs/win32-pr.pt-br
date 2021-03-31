---
title: Método Unload
description: Método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640753"
---
# <a name="unload-method"></a><span data-ttu-id="1c16a-103">Método Unload</span><span class="sxs-lookup"><span data-stu-id="1c16a-103">Unload Method</span></span>

<span data-ttu-id="1c16a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1c16a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1c16a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="1c16a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1c16a-106">Descarrega os dados de caractere para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="1c16a-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="1c16a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="1c16a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1c16a-108">*agente do ***. Caracteres. Unload "*** characterid \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="1c16a-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c16a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c16a-109">Remarks</span></span>

<span data-ttu-id="1c16a-110">Use esse método quando não precisar mais de um caractere, para liberar memória usada para armazenar informações sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="1c16a-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="1c16a-111">Se você acessar o caractere novamente, use o método [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="1c16a-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="1c16a-112">Esse método não retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="1c16a-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 