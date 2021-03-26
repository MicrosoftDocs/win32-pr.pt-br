---
description: Indica se um endereço de rede está de acordo com um tipo e formato especificados.
title: Mensagem de NCM_GETADDRESS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967482"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="4a857-103">\_Mensagem de GETendereço do NCM</span><span class="sxs-lookup"><span data-stu-id="4a857-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="4a857-104">Indica se um endereço de rede está de acordo com um tipo e formato especificados.</span><span class="sxs-lookup"><span data-stu-id="4a857-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="4a857-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a857-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a857-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a857-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a857-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4a857-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a857-108">*VP* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4a857-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="4a857-109">Um ponteiro para uma estrutura de <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> para receber informações de endereço de rede no formulário analisado, se o formato de endereço e o tipo no controle especificado por *HWND* forem validados.</span><span class="sxs-lookup"><span data-stu-id="4a857-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="4a857-110">O aplicativo de chamada é responsável por alocar a memória para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="4a857-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a857-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a857-111">Return value</span></span>

<span data-ttu-id="4a857-112">Retorna um dos seguintes valores do tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4a857-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="4a857-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4a857-113">Return code</span></span>                                                                                                | <span data-ttu-id="4a857-114">Description</span><span class="sxs-lookup"><span data-stu-id="4a857-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a857-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="4a857-116">Falha do aplicativo de chamada ao alocar uma estrutura de [**\_ endereço NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .</span><span class="sxs-lookup"><span data-stu-id="4a857-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="4a857-117"><dt>**ERRO \_ de \_ buffer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="4a857-118">O buffer de saída é muito pequeno para conter o endereço de rede analisado.</span><span class="sxs-lookup"><span data-stu-id="4a857-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="4a857-119"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="4a857-120">A cadeia de caracteres de endereço de rede não é de nenhum tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a857-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4a857-121"><dt>**êxito do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="4a857-122">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4a857-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="4a857-123"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="4a857-124">Não há nenhum endereço no controle de endereço de rede para validar.</span><span class="sxs-lookup"><span data-stu-id="4a857-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="4a857-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a857-125">Remarks</span></span>

<span data-ttu-id="4a857-126">Use a mensagem **NCM \_ GetAddress** para validar um endereço de rede em um controle de endereço de rede em relação a uma máscara de tipo de endereço de rede predefinida.</span><span class="sxs-lookup"><span data-stu-id="4a857-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="4a857-127">Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="4a857-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="4a857-128">Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a857-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="4a857-129">Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="4a857-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="4a857-130">Essa mensagem Obtém a cadeia de caracteres de endereço de rede de um controle de endereço de rede, analisa a cadeia de caracteres e verifica se a cadeia de caracteres corresponde a uma máscara de tipo de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="4a857-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="4a857-131">Se a cadeia de caracteres corresponder à máscara, a mensagem retornará S \_ OK e retornará a cadeia de caracteres no formulário analisado para o aplicativo de chamada (incluindo o número da porta, o comprimento do prefixo e outras informações de endereço), usando a estrutura de [**\_ endereço do NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) apontada por *VP*.</span><span class="sxs-lookup"><span data-stu-id="4a857-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="4a857-132">Essa mensagem retornará E \_ INVALIDARG se o aplicativo de chamada falhar ao alocar a estrutura apontada por *VP*.</span><span class="sxs-lookup"><span data-stu-id="4a857-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="4a857-133">As representações de endereço IP, versões 4 e 6 (V4/V6) para serviços e redes, bem como endereços e serviços de Internet nomeados usando o formato DNS (sistema de nomes de domínio) são analisadas.</span><span class="sxs-lookup"><span data-stu-id="4a857-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="4a857-134">Se a cadeia de caracteres de endereço de rede representar um nome de host (DNS) ou serviço nomeado, o valor retornado no membro **PrefixLength** do [**\_ endereço NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) será zero.</span><span class="sxs-lookup"><span data-stu-id="4a857-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="4a857-135">Defina a máscara de tipo de endereço de rede usando a mensagem [**NCM \_ SetAllowType**](ncm-setallowtype.md) antes de enviar a macro **\_ GetAddress NCM** .</span><span class="sxs-lookup"><span data-stu-id="4a857-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a857-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a857-136">Requirements</span></span>



| <span data-ttu-id="4a857-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a857-137">Requirement</span></span> | <span data-ttu-id="4a857-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4a857-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a857-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a857-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4a857-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a857-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a857-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a857-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4a857-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a857-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a857-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a857-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a857-144"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a857-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a857-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a857-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a857-146">**NCM \_ GETallowtype**</span><span class="sxs-lookup"><span data-stu-id="4a857-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="4a857-147">**Getendereço GetAddr \_**</span><span class="sxs-lookup"><span data-stu-id="4a857-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




