---
description: Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.
title: Mensagem de NCM_GETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010605"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="59fce-103">\_Mensagem NCM GETallowtype</span><span class="sxs-lookup"><span data-stu-id="59fce-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="59fce-104">Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.</span><span class="sxs-lookup"><span data-stu-id="59fce-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="59fce-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59fce-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fce-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59fce-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59fce-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="59fce-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59fce-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59fce-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59fce-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="59fce-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fce-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59fce-110">Return value</span></span>

<span data-ttu-id="59fce-111">Retorna os tipos de endereço de rede permitidos como uma ou mais constantes de [**\_ cadeia de caracteres net**](net-string.md) .</span><span class="sxs-lookup"><span data-stu-id="59fce-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="59fce-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="59fce-112">Remarks</span></span>

<span data-ttu-id="59fce-113">A máscara retornada é o critério usado para validar um endereço de rede na mensagem [**NCM \_ GetAddress**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="59fce-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="59fce-114">Use esta mensagem somente para um controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="59fce-114">Use this message for a network address control only.</span></span> <span data-ttu-id="59fce-115">Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="59fce-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="59fce-116">Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="59fce-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="59fce-117">Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="59fce-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="59fce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59fce-118">Requirements</span></span>



| <span data-ttu-id="59fce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="59fce-119">Requirement</span></span> | <span data-ttu-id="59fce-120">Valor</span><span class="sxs-lookup"><span data-stu-id="59fce-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59fce-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59fce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59fce-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59fce-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59fce-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59fce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59fce-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59fce-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59fce-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59fce-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="59fce-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59fce-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59fce-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="59fce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fce-128">**NCM \_ SETallowtype**</span><span class="sxs-lookup"><span data-stu-id="59fce-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="59fce-129">**Getallowtype de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="59fce-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




