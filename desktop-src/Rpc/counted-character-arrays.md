---
title: Matrizes de caracteres contadas
description: O atributo \ Size \_ is \ indica o limite superior da matriz, enquanto o atributo \ length \_ is \ indica o número de elementos da matriz a serem transmitidos.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454197"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="a01b5-103">Matrizes de caracteres contadas</span><span class="sxs-lookup"><span data-stu-id="a01b5-103">Counted Character Arrays</span></span>

<span data-ttu-id="a01b5-104">O \[ atributo [Size \_ é](/windows/desktop/Midl/size-is) \] indica o limite superior da matriz, enquanto o \[ [comprimento \_ é](/windows/desktop/Midl/length-is) \] atributo indica o número de elementos da matriz a serem transmitidos.</span><span class="sxs-lookup"><span data-stu-id="a01b5-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="a01b5-105">Além da matriz, o protótipo de procedimento remoto deve incluir todas as variáveis que representam o comprimento ou o tamanho que determinam os elementos da matriz transmitida (eles podem ser parâmetros separados ou agrupados com a cadeia de caracteres em uma estrutura).</span><span class="sxs-lookup"><span data-stu-id="a01b5-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="a01b5-106">Esses atributos podem ser usados com matrizes de caracteres largos ou de byte único da mesma forma que seriam com matrizes de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="a01b5-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="a01b5-107">As informações nesta seção descrevem os protótipos de parâmetro de procedimento remoto para matrizes de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a01b5-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="a01b5-108">Ele é dividido nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a01b5-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="a01b5-109">[\[in, out, o tamanho \_ é \] protótipo](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="a01b5-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="a01b5-110">[\[em, tamanho \_ é e out, o tamanho \_ é \] protótipo](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="a01b5-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 