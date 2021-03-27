---
description: Define os tipos de endereço de rede que um controle de endereço de rede especificado aceita.
title: Mensagem de NCM_SETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647538"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="87a4a-103">\_Mensagem NCM SETallowtype</span><span class="sxs-lookup"><span data-stu-id="87a4a-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="87a4a-104">Define os tipos de endereço de rede que um controle de endereço de rede especificado aceita.</span><span class="sxs-lookup"><span data-stu-id="87a4a-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="87a4a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87a4a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a4a-106">*addrMask* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87a4a-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="87a4a-107">Especifica os tipos de endereço de rede como uma ou mais constantes de <a href="net-string.md">**\_ cadeia de caracteres net**</a> .</span><span class="sxs-lookup"><span data-stu-id="87a4a-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="87a4a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87a4a-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87a4a-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="87a4a-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a4a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87a4a-110">Return value</span></span>

<span data-ttu-id="87a4a-111">Retorna S \_ OK se for bem-sucedido, ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="87a4a-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a4a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="87a4a-112">Remarks</span></span>

<span data-ttu-id="87a4a-113">O conjunto de máscaras é o critério usado para validar um endereço de rede na mensagem [**NCM \_ GetAddress**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="87a4a-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="87a4a-114">Use esta mensagem somente para um controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="87a4a-114">Use this message for a network address control only.</span></span> <span data-ttu-id="87a4a-115">Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="87a4a-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="87a4a-116">Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="87a4a-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="87a4a-117">Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="87a4a-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a4a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a4a-118">Requirements</span></span>



| <span data-ttu-id="87a4a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a4a-119">Requirement</span></span> | <span data-ttu-id="87a4a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="87a4a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87a4a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87a4a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87a4a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87a4a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87a4a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87a4a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87a4a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87a4a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87a4a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87a4a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87a4a-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="87a4a-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a4a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="87a4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a4a-128">**NCM \_ GETallowtype**</span><span class="sxs-lookup"><span data-stu-id="87a4a-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="87a4a-129">**SetAllowType de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="87a4a-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




