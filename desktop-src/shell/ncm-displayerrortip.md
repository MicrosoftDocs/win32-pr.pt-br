---
description: Exibe uma mensagem de erro na dica de balão associada ao controle de endereço de rede.
title: Mensagem de NCM_DISPLAYERRORTIP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988757"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="1ad2f-103">\_Mensagem NCM DISPLAYERRORTIP</span><span class="sxs-lookup"><span data-stu-id="1ad2f-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="1ad2f-104">Exibe uma mensagem de erro na dica de balão associada ao controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="1ad2f-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="1ad2f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ad2f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad2f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ad2f-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ad2f-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ad2f-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ad2f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ad2f-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ad2f-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ad2f-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad2f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ad2f-110">Return value</span></span>

<span data-ttu-id="1ad2f-111">Se essa mensagem tiver sucesso, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1ad2f-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ad2f-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ad2f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad2f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ad2f-113">Remarks</span></span>

<span data-ttu-id="1ad2f-114">Envie esta mensagem para exibir uma mensagem de erro quando um endereço digitado no controle não for validado em relação aos tipos de endereço de rede permitidos definidos com a mensagem [**NCM \_**](ncm-setallowtype.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad2f-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="1ad2f-115">Use a mensagem [**NCM \_ GetAddress**](ncm-getaddress.md) para validar o endereço.</span><span class="sxs-lookup"><span data-stu-id="1ad2f-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad2f-116">Requirements</span></span>



| <span data-ttu-id="1ad2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ad2f-117">Requirement</span></span> | <span data-ttu-id="1ad2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1ad2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad2f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ad2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad2f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ad2f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ad2f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ad2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad2f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ad2f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ad2f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ad2f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad2f-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad2f-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad2f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ad2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad2f-126">**DisplayErrorTip de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="1ad2f-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




