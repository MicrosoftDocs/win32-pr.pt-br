---
title: Mensagem de UDM_SETBASE (commctrl. h)
description: Define a base do Radix para um controle de cima para baixo. O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais. Os números hexadecimais são sempre não assinados e números decimais são assinados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Controles de UDM_SETBASE de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918773"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="8df15-106">Mensagem do UDM \_ SETbase</span><span class="sxs-lookup"><span data-stu-id="8df15-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="8df15-107">Define a base do Radix para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="8df15-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="8df15-108">O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="8df15-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="8df15-109">Os números hexadecimais são sempre não assinados e números decimais são assinados.</span><span class="sxs-lookup"><span data-stu-id="8df15-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="8df15-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8df15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df15-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8df15-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8df15-112">Novo valor base para o controle.</span><span class="sxs-lookup"><span data-stu-id="8df15-112">New base value for the control.</span></span> <span data-ttu-id="8df15-113">Esse parâmetro pode ser 10 para decimal ou 16 para hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="8df15-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="8df15-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8df15-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8df15-115">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8df15-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df15-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8df15-116">Return value</span></span>

<span data-ttu-id="8df15-117">O valor de retorno é o valor base anterior.</span><span class="sxs-lookup"><span data-stu-id="8df15-117">The return value is the previous base value.</span></span> <span data-ttu-id="8df15-118">Se uma base inválida for fornecida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="8df15-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df15-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8df15-119">Requirements</span></span>



| <span data-ttu-id="8df15-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df15-120">Requirement</span></span> | <span data-ttu-id="8df15-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8df15-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8df15-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8df15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8df15-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8df15-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8df15-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8df15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8df15-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8df15-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8df15-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8df15-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df15-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df15-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





