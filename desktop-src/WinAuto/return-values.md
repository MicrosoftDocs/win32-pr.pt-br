---
title: Valores de retorno (recursos de acessibilidade do Windows)
description: Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que você pode ver com menos frequência.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443987"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="12cf4-103">Valores de retorno (recursos de acessibilidade do Windows)</span><span class="sxs-lookup"><span data-stu-id="12cf4-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="12cf4-104">Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que você pode ver com menos frequência.</span><span class="sxs-lookup"><span data-stu-id="12cf4-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="12cf4-105">Valores de retorno comuns</span><span class="sxs-lookup"><span data-stu-id="12cf4-105">Common Return Values</span></span>

<span data-ttu-id="12cf4-106">Os [**métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retornam um dos seguintes valores, definidos em winerror.h ou outro código de erro COM (Component Object Model padrão:</span><span class="sxs-lookup"><span data-stu-id="12cf4-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="12cf4-107">Valor</span><span class="sxs-lookup"><span data-stu-id="12cf4-107">Value</span></span>                      |   <span data-ttu-id="12cf4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="12cf4-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12cf4-109">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="12cf4-109">S\_OK</span></span>                   | <span data-ttu-id="12cf4-110">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="12cf4-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="12cf4-111">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="12cf4-111">S\_FALSE</span></span>                | <span data-ttu-id="12cf4-112">O método foi bem-sucedido em parte.</span><span class="sxs-lookup"><span data-stu-id="12cf4-112">The method succeeded in part.</span></span> <span data-ttu-id="12cf4-113">Isso acontece quando o método é bem-sucedido, mas as informações solicitadas não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12cf4-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="12cf4-114">Por exemplo, Microsoft Active Accessibility retornará S FALSE se você chamar \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar um objeto filho em um determinado ponto e o ponto especificado não estiver dentro do objeto ou do filho do objeto.</span><span class="sxs-lookup"><span data-stu-id="12cf4-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="12cf4-115">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="12cf4-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="12cf4-116">O objeto não dá suporte à propriedade ou ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="12cf4-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="12cf4-117">Por exemplo, um botão de push retornará esse valor se você solicitar sua [propriedade Value](value-property.md), porque ele não tem uma propriedade Value.</span><span class="sxs-lookup"><span data-stu-id="12cf4-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="12cf4-118">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="12cf4-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="12cf4-119">O método não é implementado.</span><span class="sxs-lookup"><span data-stu-id="12cf4-119">The method is not implemented.</span></span> <span data-ttu-id="12cf4-120">Esse valor ocorre quando um cliente chama um método que ainda não tem suporte nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="12cf4-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="12cf4-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12cf4-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="12cf4-122">Um ou mais argumentos não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="12cf4-122">One or more arguments were not valid.</span></span> <span data-ttu-id="12cf4-123">Esse erro ocorre quando o chamador tenta identificar um objeto filho usando um identificador que o servidor não reconhece.</span><span class="sxs-lookup"><span data-stu-id="12cf4-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="12cf4-124">Esse erro também resulta quando um cliente tenta identificar um objeto filho dentro de um objeto que não tem filhos.</span><span class="sxs-lookup"><span data-stu-id="12cf4-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="12cf4-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="12cf4-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="12cf4-126">O método não pôde alocar memória necessária para concluir uma operação crucial para seu sucesso.</span><span class="sxs-lookup"><span data-stu-id="12cf4-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="12cf4-127">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="12cf4-127">E\_FAIL</span></span>                 | <span data-ttu-id="12cf4-128">Ocorreu um erro desconhecido ou genérico.</span><span class="sxs-lookup"><span data-stu-id="12cf4-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="12cf4-129">Valores de retorno adicionais</span><span class="sxs-lookup"><span data-stu-id="12cf4-129">Additional Return Values</span></span>

<span data-ttu-id="12cf4-130">A seguir estão os valores de retorno [**que os métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) podem retornar.</span><span class="sxs-lookup"><span data-stu-id="12cf4-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="12cf4-131">Esses valores de retorno não são tão comuns quanto os anteriores, mas você deve estar ciente deles.</span><span class="sxs-lookup"><span data-stu-id="12cf4-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="12cf4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="12cf4-132">Value</span></span>                    |    <span data-ttu-id="12cf4-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="12cf4-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12cf4-134">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="12cf4-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="12cf4-135">Isso é retornado quando você chama get \_ accValue para obter o valor de um controle de senha.</span><span class="sxs-lookup"><span data-stu-id="12cf4-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="12cf4-136">EXCEÇÃO \_ DISP E \_</span><span class="sxs-lookup"><span data-stu-id="12cf4-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="12cf4-137">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="12cf4-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




