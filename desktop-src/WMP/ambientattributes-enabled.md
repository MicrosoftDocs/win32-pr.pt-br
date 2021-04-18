---
title: Ambienteattributes. habilitado
description: O atributo Enabled especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Ambiente do Windows Media Player habilitado para ambientes.
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784922"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="20514-104">Ambienteattributes. habilitado</span><span class="sxs-lookup"><span data-stu-id="20514-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="20514-105">O atributo **Enabled** especifica ou recupera um valor que indica se o controle está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="20514-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="20514-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="20514-106">Possible Values</span></span>

<span data-ttu-id="20514-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="20514-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="20514-108">Valor</span><span class="sxs-lookup"><span data-stu-id="20514-108">Value</span></span> | <span data-ttu-id="20514-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="20514-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="20514-110">true</span><span class="sxs-lookup"><span data-stu-id="20514-110">true</span></span>  | <span data-ttu-id="20514-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="20514-111">Default.</span></span> <span data-ttu-id="20514-112">Controle habilitado.</span><span class="sxs-lookup"><span data-stu-id="20514-112">Control enabled.</span></span> |
| <span data-ttu-id="20514-113">false</span><span class="sxs-lookup"><span data-stu-id="20514-113">false</span></span> | <span data-ttu-id="20514-114">Controle desabilitado.</span><span class="sxs-lookup"><span data-stu-id="20514-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="20514-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="20514-115">Remarks</span></span>

<span data-ttu-id="20514-116">Se o controle estiver habilitado, ele poderá ter uma parada de tabulação e receberá todos os eventos de ambiente.</span><span class="sxs-lookup"><span data-stu-id="20514-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="20514-117">Quando desabilitado, o controle não tem uma parada de tabulação e não recebe nenhum evento de teclado ou mouse de ambiente acionado para ele.</span><span class="sxs-lookup"><span data-stu-id="20514-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="20514-118">(No entanto, ele continuará a receber todos os outros eventos de ambiente acionados para ele.)</span><span class="sxs-lookup"><span data-stu-id="20514-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="20514-119">Não há suporte para esse atributo no elemento **subview** .</span><span class="sxs-lookup"><span data-stu-id="20514-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="20514-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20514-120">Requirements</span></span>



| <span data-ttu-id="20514-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20514-121">Requirement</span></span> | <span data-ttu-id="20514-122">Valor</span><span class="sxs-lookup"><span data-stu-id="20514-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="20514-123">Versão</span><span class="sxs-lookup"><span data-stu-id="20514-123">Version</span></span><br/> | <span data-ttu-id="20514-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="20514-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20514-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="20514-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20514-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="20514-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





