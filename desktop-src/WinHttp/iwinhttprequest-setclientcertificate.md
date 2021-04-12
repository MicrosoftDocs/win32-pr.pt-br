---
description: Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Método IWinHttpRequest:: SetClientCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297090"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="988dc-103">Método IWinHttpRequest:: SetClientCertificate</span><span class="sxs-lookup"><span data-stu-id="988dc-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="988dc-104">O método **SetClientCertificate** seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.</span><span class="sxs-lookup"><span data-stu-id="988dc-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="988dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="988dc-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="988dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="988dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988dc-107">*ClientCertificate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="988dc-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="988dc-108">Especifica o local, o [*repositório de certificados*](glossary.md)e o assunto de um certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="988dc-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988dc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="988dc-109">Return value</span></span>

<span data-ttu-id="988dc-110">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="988dc-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="988dc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="988dc-111">Remarks</span></span>

<span data-ttu-id="988dc-112">A cadeia de caracteres especificada no parâmetro *ClientCertificate* consiste no local do certificado, no repositório de certificados e no nome da entidade delimitada por barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="988dc-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="988dc-113">Para obter mais informações sobre os componentes da cadeia de caracteres do certificado, consulte [certificados do cliente](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="988dc-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="988dc-114">O nome e o local do repositório de certificados são opcionais.</span><span class="sxs-lookup"><span data-stu-id="988dc-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="988dc-115">No entanto, se você especificar um repositório de certificados, também deverá especificar o local desse repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="988dc-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="988dc-116">O local padrão é o \_ usuário atual e o repositório de certificados padrão é "My".</span><span class="sxs-lookup"><span data-stu-id="988dc-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="988dc-117">Um assunto em branco indica que o primeiro certificado no repositório de certificados deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="988dc-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="988dc-118">Chame **SetClientCertificate** para selecionar um certificado antes de chamar [**Send**](iwinhttprequest-send.md) para enviar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="988dc-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="988dc-119">O Microsoft Windows HTTP Services (WinHTTP) não fornece certificados de cliente para servidores proxy que solicitam certificados para autenticação.</span><span class="sxs-lookup"><span data-stu-id="988dc-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="988dc-120">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="988dc-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="988dc-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="988dc-121">Examples</span></span>

<span data-ttu-id="988dc-122">O exemplo de script a seguir mostra como selecionar um certificado de cliente para enviar com uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="988dc-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="988dc-123">Um certificado com o assunto "meu certificado de Middle-Tier" é escolhido no repositório de certificados "pessoal" no registro em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="988dc-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="988dc-124">Como este exemplo de código é específico do Microsoft JScript, que usa a barra invertida como um caractere de escape, duas barras invertidas adjacentes são necessárias para delimitar os componentes da cadeia de caracteres do certificado.</span><span class="sxs-lookup"><span data-stu-id="988dc-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="988dc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="988dc-125">Requirements</span></span>



| <span data-ttu-id="988dc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="988dc-126">Requirement</span></span> | <span data-ttu-id="988dc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="988dc-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="988dc-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="988dc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="988dc-129">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="988dc-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="988dc-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="988dc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="988dc-131">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="988dc-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="988dc-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="988dc-132">Redistributable</span></span><br/>          | <span data-ttu-id="988dc-133">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="988dc-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="988dc-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="988dc-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="988dc-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="988dc-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="988dc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="988dc-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="988dc-137"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="988dc-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="988dc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="988dc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="988dc-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="988dc-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="988dc-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="988dc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988dc-141">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="988dc-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="988dc-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="988dc-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="988dc-143">SSL no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="988dc-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="988dc-144">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="988dc-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




