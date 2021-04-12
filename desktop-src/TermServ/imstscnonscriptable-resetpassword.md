---
title: Método IMsTscNonScriptable ResetPassword
description: Redefine todos os Estados de senha no controle ActiveX Área de Trabalho Remota.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ResetPassword
- Método ResetPassword Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, método ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455868"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="f9475-106">Método IMsTscNonScriptable:: ResetPassword</span><span class="sxs-lookup"><span data-stu-id="f9475-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="f9475-107">Redefine todos os Estados de senha no controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f9475-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="f9475-108">Você pode chamar esse método para limpar as senhas que são armazenadas em qualquer um dos três formatos com suporte: texto não criptografado, codificado em Portable ou binário (não Portable).</span><span class="sxs-lookup"><span data-stu-id="f9475-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="f9475-109">Observe que as senhas codificadas não devem ser consideradas criptografadas com segurança.</span><span class="sxs-lookup"><span data-stu-id="f9475-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9475-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9475-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="f9475-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9475-111">Parameters</span></span>

<span data-ttu-id="f9475-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f9475-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9475-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9475-113">Return value</span></span>

<span data-ttu-id="f9475-114">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f9475-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9475-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9475-115">Remarks</span></span>

<span data-ttu-id="f9475-116">Você pode chamar esse método para redefinir a senha do controle após a desconexão.</span><span class="sxs-lookup"><span data-stu-id="f9475-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="f9475-117">Isso garante que as conexões subsequentes que usam a mesma instância do controle não façam logon automaticamente com uma senha definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f9475-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="f9475-118">Você só pode chamar esse método quando o controle ActiveX Área de Trabalho Remota não está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="f9475-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="f9475-119">Esse método retorna **E \_ falha** se chamado quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="f9475-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="f9475-120">Para verificar o estado conectado, chame o método [**Get \_ conectado**](imstscax-connected.md) por meio da interface [**IMsTscAx**](imstscax-interface.md) ou uma das interfaces herdadas dele.</span><span class="sxs-lookup"><span data-stu-id="f9475-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="f9475-121">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f9475-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9475-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9475-122">Requirements</span></span>



| <span data-ttu-id="f9475-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9475-123">Requirement</span></span> | <span data-ttu-id="f9475-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f9475-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9475-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9475-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f9475-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9475-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f9475-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9475-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f9475-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9475-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f9475-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9475-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9475-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9475-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9475-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f9475-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9475-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9475-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9475-133">IID</span><span class="sxs-lookup"><span data-stu-id="f9475-133">IID</span></span><br/>                      | <span data-ttu-id="f9475-134">IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="f9475-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9475-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9475-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9475-136">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="f9475-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





