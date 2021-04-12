---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453986"
---
# <a name="gestureat-method"></a><span data-ttu-id="433f2-103">Método GestureAt</span><span class="sxs-lookup"><span data-stu-id="433f2-103">GestureAt Method</span></span>

<span data-ttu-id="433f2-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="433f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="433f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="433f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="433f2-106">Reproduz a animação gesturing para o caractere especificado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="433f2-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="433f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="433f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="433f2-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). GestureAt* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="433f2-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="433f2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="433f2-109">Part</span></span>  | <span data-ttu-id="433f2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="433f2-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433f2-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="433f2-111">*x,y*</span></span> | <span data-ttu-id="433f2-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="433f2-112">Required.</span></span> <span data-ttu-id="433f2-113">Um valor inteiro que indica a coordenada de tela horizontal (*x*) e a coordenada de tela vertical (*y*) para a qual o caractere será gestodo.</span><span class="sxs-lookup"><span data-stu-id="433f2-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="433f2-114">Essas coordenadas devem ser especificadas em pixels.</span><span class="sxs-lookup"><span data-stu-id="433f2-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="433f2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="433f2-115">Remarks</span></span>

<span data-ttu-id="433f2-116">O servidor desempenha automaticamente a animação apropriada para gestor em direção ao local especificado.</span><span class="sxs-lookup"><span data-stu-id="433f2-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="433f2-117">As coordenadas são sempre relativas à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="433f2-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="433f2-118">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="433f2-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="433f2-119">Além disso, se a animação associada não tiver sido carregada no computador local, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="433f2-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="433f2-120">Portanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar as animações de estado **gesturing** antes de chamar o método **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="433f2-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 