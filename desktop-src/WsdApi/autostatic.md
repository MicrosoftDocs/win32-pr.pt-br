---
description: Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autoestático
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994923"
---
# <a name="autostatic-element"></a><span data-ttu-id="1d5c7-103">elemento autoestático</span><span class="sxs-lookup"><span data-stu-id="1d5c7-103">autoStatic element</span></span>

<span data-ttu-id="1d5c7-104">Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="1d5c7-105">Esse comportamento é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="1d5c7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="1d5c7-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="1d5c7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d5c7-107">Attributes</span></span>

<span data-ttu-id="1d5c7-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1d5c7-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1d5c7-109">Child elements</span></span>

<span data-ttu-id="1d5c7-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1d5c7-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1d5c7-111">Parent elements</span></span>



| <span data-ttu-id="1d5c7-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d5c7-112">Element</span></span>                                     | <span data-ttu-id="1d5c7-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d5c7-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d5c7-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="1d5c7-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="1d5c7-115">O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1d5c7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d5c7-116">Remarks</span></span>

<span data-ttu-id="1d5c7-117">O elemento **autostatic** não é obrigatório e pode ser omitido do arquivo de configuração XML.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="1d5c7-118">O elemento pode ser usado para desabilitar a sinalização de campos gerados como estático ou para forçar explicitamente a sinalização de determinados campos gerados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="1d5c7-119">Os valores possíveis são 1 (habilitado, padrão) e 0 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="1d5c7-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="1d5c7-120">Habilitar o **autostatic** pode causar problemas de compilação dependendo de como o gerador de código é direcionado para os dados de saída.</span><span class="sxs-lookup"><span data-stu-id="1d5c7-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="1d5c7-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1d5c7-121">Element information</span></span>



| <span data-ttu-id="1d5c7-122">Label</span><span class="sxs-lookup"><span data-stu-id="1d5c7-122">Label</span></span> | <span data-ttu-id="1d5c7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1d5c7-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="1d5c7-124">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d5c7-124">Minimum supported system</span></span><br/> | <span data-ttu-id="1d5c7-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d5c7-125">Windows Vista</span></span> |
| <span data-ttu-id="1d5c7-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="1d5c7-126">Can be empty</span></span>                        | <span data-ttu-id="1d5c7-127">Sim</span><span class="sxs-lookup"><span data-stu-id="1d5c7-127">Yes</span></span>           |



 

 




