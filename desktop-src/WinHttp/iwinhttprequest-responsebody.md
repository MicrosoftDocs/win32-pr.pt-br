---
description: Recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Propriedade IWinHttpRequest:: ResponseBody'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763074"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="330e7-103">Propriedade IWinHttpRequest:: ResponseBody</span><span class="sxs-lookup"><span data-stu-id="330e7-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="330e7-104">A propriedade **responseBody** recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="330e7-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="330e7-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="330e7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="330e7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="330e7-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="330e7-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="330e7-107">Property value</span></span>

<span data-ttu-id="330e7-108">Um valor **Variant** que recebe o corpo da entidade de resposta como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="330e7-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="330e7-109">Essa matriz contém os dados brutos como recebidos diretamente do servidor.</span><span class="sxs-lookup"><span data-stu-id="330e7-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="330e7-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="330e7-110">Error codes</span></span>

<span data-ttu-id="330e7-111">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="330e7-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="330e7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="330e7-112">Remarks</span></span>

<span data-ttu-id="330e7-113">Essa propriedade retorna os dados de resposta em uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="330e7-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="330e7-114">Se a resposta não tiver um corpo de resposta, uma variante vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="330e7-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="330e7-115">Essa propriedade só pode ser chamada depois que o método [**Send**](iwinhttprequest-send.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="330e7-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="330e7-116">Para obter mais informações sobre a implementação do Windows XP e do Windows 2000, consulte [requisitos de tempo de execução](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="330e7-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="330e7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330e7-117">Requirements</span></span>



| <span data-ttu-id="330e7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="330e7-118">Requirement</span></span> | <span data-ttu-id="330e7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="330e7-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="330e7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="330e7-121">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="330e7-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="330e7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="330e7-123">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="330e7-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="330e7-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="330e7-124">Redistributable</span></span><br/>          | <span data-ttu-id="330e7-125">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="330e7-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="330e7-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="330e7-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="330e7-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="330e7-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="330e7-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="330e7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="330e7-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="330e7-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="330e7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="330e7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="330e7-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="330e7-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="330e7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="330e7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330e7-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="330e7-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="330e7-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="330e7-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="330e7-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="330e7-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="330e7-136">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="330e7-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="330e7-137">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="330e7-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




