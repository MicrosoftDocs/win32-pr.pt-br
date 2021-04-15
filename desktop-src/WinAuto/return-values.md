---
title: Valores de retorno (recursos de acessibilidade do Windows)
description: Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que podem ser exibidos com menos frequência.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454498"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="c475a-103">Valores de retorno (recursos de acessibilidade do Windows)</span><span class="sxs-lookup"><span data-stu-id="c475a-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="c475a-104">Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que podem ser exibidos com menos frequência.</span><span class="sxs-lookup"><span data-stu-id="c475a-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="c475a-105">Valores de retorno comuns</span><span class="sxs-lookup"><span data-stu-id="c475a-105">Common Return Values</span></span>

<span data-ttu-id="c475a-106">Os métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retornam um dos seguintes valores, definidos em Winerror. h ou outro código de erro de Component Object Model padrão (com):</span><span class="sxs-lookup"><span data-stu-id="c475a-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c475a-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="c475a-107">S\_OK</span></span>                   | <span data-ttu-id="c475a-108">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c475a-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c475a-109">\_falso</span><span class="sxs-lookup"><span data-stu-id="c475a-109">S\_FALSE</span></span>                | <span data-ttu-id="c475a-110">O método foi bem-sucedido na parte.</span><span class="sxs-lookup"><span data-stu-id="c475a-110">The method succeeded in part.</span></span> <span data-ttu-id="c475a-111">Isso acontece quando o método é executado com sucesso, mas as informações solicitadas não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c475a-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="c475a-112">Por exemplo, Microsoft Acessibilidade Ativa retornará S \_ false se você chamar [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar um objeto filho em um determinado ponto e o ponto especificado não estiver dentro do objeto ou do filho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c475a-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="c475a-113">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="c475a-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="c475a-114">O objeto não oferece suporte à propriedade ou ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="c475a-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="c475a-115">Por exemplo, um botão de ação retorna esse valor se você solicitar sua [propriedade Value](value-property.md), porque ela não tem uma propriedade Value.</span><span class="sxs-lookup"><span data-stu-id="c475a-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="c475a-116">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c475a-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="c475a-117">O método não está implementado.</span><span class="sxs-lookup"><span data-stu-id="c475a-117">The method is not implemented.</span></span> <span data-ttu-id="c475a-118">Esse valor ocorre quando um cliente chama um método que ainda não tem suporte nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c475a-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c475a-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c475a-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="c475a-120">Um ou mais argumentos não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="c475a-120">One or more arguments were not valid.</span></span> <span data-ttu-id="c475a-121">Esse erro ocorre quando o chamador tenta identificar um objeto filho usando um identificador que o servidor não reconhece.</span><span class="sxs-lookup"><span data-stu-id="c475a-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="c475a-122">Esse erro também ocorre quando um cliente tenta identificar um objeto filho dentro de um objeto que não tem filhos.</span><span class="sxs-lookup"><span data-stu-id="c475a-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="c475a-123">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c475a-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="c475a-124">O método não pôde alocar memória necessária para concluir uma operação crucial para seu sucesso.</span><span class="sxs-lookup"><span data-stu-id="c475a-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c475a-125">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="c475a-125">E\_FAIL</span></span>                 | <span data-ttu-id="c475a-126">Ocorreu um erro desconhecido ou genérico.</span><span class="sxs-lookup"><span data-stu-id="c475a-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="c475a-127">Valores de retorno adicionais</span><span class="sxs-lookup"><span data-stu-id="c475a-127">Additional Return Values</span></span>

<span data-ttu-id="c475a-128">Os seguintes são valores de retorno que os métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) podem retornar.</span><span class="sxs-lookup"><span data-stu-id="c475a-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="c475a-129">Esses valores de retorno não são tão comuns quanto os anteriores, mas você deve estar ciente deles.</span><span class="sxs-lookup"><span data-stu-id="c475a-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c475a-130">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="c475a-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="c475a-131">Isso é retornado quando você chama get \_ accValue para obter o valor de um controle de senha.</span><span class="sxs-lookup"><span data-stu-id="c475a-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="c475a-132">obter \_ E \_ exceção</span><span class="sxs-lookup"><span data-stu-id="c475a-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="c475a-133">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="c475a-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




