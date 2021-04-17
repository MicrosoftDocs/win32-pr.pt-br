---
description: Define a política de logon automático atual.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Método IWinHttpRequest:: SetAutoLogonPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780306"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="f8bbf-103">Método IWinHttpRequest:: SetAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="f8bbf-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="f8bbf-104">O método **SetAutoLogonPolicy** define a [política de logon automático](authentication-in-winhttp.md)atual.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bbf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8bbf-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="f8bbf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8bbf-107">*AutoLogonPolicy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8bbf-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8bbf-108">Especifica a política de logon automático atual.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8bbf-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8bbf-109">Return value</span></span>

<span data-ttu-id="f8bbf-110">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8bbf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8bbf-111">Remarks</span></span>

<span data-ttu-id="f8bbf-112">A política padrão é [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f8bbf-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="f8bbf-113">Chame **SetAutoLogonPolicy** para definir a política de logon automática antes de chamar [**Send**](iwinhttprequest-send.md) para enviar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="f8bbf-114">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f8bbf-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8bbf-115">Examples</span></span>

<span data-ttu-id="f8bbf-116">O exemplo de script a seguir mostra como definir a política de logon automático para nunca usar a autenticação NTLM ou negociar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="f8bbf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8bbf-117">Requirements</span></span>



| <span data-ttu-id="f8bbf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8bbf-118">Requirement</span></span> | <span data-ttu-id="f8bbf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f8bbf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bbf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8bbf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bbf-121">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f8bbf-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="f8bbf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8bbf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bbf-123">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f8bbf-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="f8bbf-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f8bbf-124">Redistributable</span></span><br/>          | <span data-ttu-id="f8bbf-125">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f8bbf-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="f8bbf-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="f8bbf-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8bbf-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8bbf-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="f8bbf-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8bbf-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8bbf-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8bbf-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="f8bbf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f8bbf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8bbf-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8bbf-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f8bbf-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8bbf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8bbf-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f8bbf-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="f8bbf-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f8bbf-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="f8bbf-135">Autenticação no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f8bbf-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="f8bbf-136">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f8bbf-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




