---
title: Mostrar método
description: Mostrar método
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105760604"
---
# <a name="show-method"></a><span data-ttu-id="af8ff-103">Mostrar método</span><span class="sxs-lookup"><span data-stu-id="af8ff-103">Show Method</span></span>

<span data-ttu-id="af8ff-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af8ff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af8ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="af8ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af8ff-106">Torna o caractere especificado visível e executa sua animação de **exibição** associada.</span><span class="sxs-lookup"><span data-stu-id="af8ff-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="af8ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="af8ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="af8ff-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Mostrar* \*  \[ *rápido*\]</span><span class="sxs-lookup"><span data-stu-id="af8ff-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="af8ff-109">Parte</span><span class="sxs-lookup"><span data-stu-id="af8ff-109">Part</span></span>   | <span data-ttu-id="af8ff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="af8ff-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af8ff-111">*Rápido*</span><span class="sxs-lookup"><span data-stu-id="af8ff-111">*Fast*</span></span> | <span data-ttu-id="af8ff-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="af8ff-112">Optional.</span></span> <span data-ttu-id="af8ff-113">Uma expressão booliana que especifica se o servidor reproduz a animação em **exibição** .</span><span class="sxs-lookup"><span data-stu-id="af8ff-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="af8ff-114">**Verdadeiro** Ignora a animação de estado de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="af8ff-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="af8ff-115">**False** (padrão) não ignora a animação de estado de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="af8ff-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af8ff-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="af8ff-116">Remarks</span></span>

<span data-ttu-id="af8ff-117">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="af8ff-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="af8ff-118">Além disso, se a animação de **exibição** associada não tiver sido carregada e você não tiver especificado o parâmetro **Fast** como **true**, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="af8ff-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="af8ff-119">Portanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação de estado de **exibição** antes de chamar o método **show** .</span><span class="sxs-lookup"><span data-stu-id="af8ff-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="af8ff-120">Evite definir o parâmetro **Fast** como **true** sem primeiro reproduzir uma animação antes; caso contrário, o quadro de caracteres poderá ser exibido sem imagem.</span><span class="sxs-lookup"><span data-stu-id="af8ff-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="af8ff-121">Em particular, observe que, se você chamar [**MoveTo**](moveto-method.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação.</span><span class="sxs-lookup"><span data-stu-id="af8ff-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="af8ff-122">Portanto, se você chamar o método **show** com **Fast** definido como **true**, nenhuma imagem será exibida.</span><span class="sxs-lookup"><span data-stu-id="af8ff-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="af8ff-123">Da mesma forma, se você chamar [**Hide**](hide-method.md) e **Mostrar** with **Fast** Set como **true**, não haverá imagem visível.</span><span class="sxs-lookup"><span data-stu-id="af8ff-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="af8ff-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="af8ff-124">See Also</span></span>

[<span data-ttu-id="af8ff-125">**Método Hide**</span><span class="sxs-lookup"><span data-stu-id="af8ff-125">**Hide method**</span></span>](hide-method.md)


 

