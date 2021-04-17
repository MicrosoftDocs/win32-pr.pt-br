---
title: Método Session. Identify (WSManDisp. h)
description: Consulta um computador remoto para determinar se ele dá suporte ao protocolo de WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método de identificação
- Gerenciamento Remoto do Windows método de identificação, objeto de sessão
- Gerenciamento Remoto do Windows de objeto de sessão, método Identify
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812095"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="30851-106">Método Session. Identify</span><span class="sxs-lookup"><span data-stu-id="30851-106">Session.Identify method</span></span>

<span data-ttu-id="30851-107">O método **Session. Identify** consulta um computador remoto para determinar se ele dá suporte ao protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="30851-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="30851-108">Para obter mais informações, consulte [detectando se um computador remoto dá suporte ao protocolo WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="30851-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30851-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30851-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="30851-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30851-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30851-111">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="30851-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30851-112">Para enviar a solicitação no modo autenticado, use a constante de autenticação da enumeração **WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="30851-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="30851-113">Para enviar em modo não autenticado, use **WSManFlagUseNoAuthentication**.</span><span class="sxs-lookup"><span data-stu-id="30851-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="30851-114">Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="30851-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30851-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30851-115">Return value</span></span>

<span data-ttu-id="30851-116">Uma cadeia de caracteres XML que especifica a versão do protocolo WS-Management, o fornecedor do sistema operacional e, se a solicitação foi enviada autenticada, a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="30851-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="30851-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="30851-117">Remarks</span></span>

<span data-ttu-id="30851-118">**Session. Identify** é baseado na operação de [protocolo WS-Management](ws-management-protocol.md) definida como wsmanIdentity.</span><span class="sxs-lookup"><span data-stu-id="30851-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="30851-119">Isso é especificado no pacote SOAP da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="30851-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="30851-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30851-120">Examples</span></span>

<span data-ttu-id="30851-121">O exemplo de VBScript a seguir envia uma solicitação de identificação não autenticada para o computador remoto chamado Remote no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="30851-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="30851-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30851-122">Requirements</span></span>



| <span data-ttu-id="30851-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30851-123">Requirement</span></span> | <span data-ttu-id="30851-124">Valor</span><span class="sxs-lookup"><span data-stu-id="30851-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30851-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30851-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30851-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30851-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="30851-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30851-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30851-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30851-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30851-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30851-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="30851-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30851-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30851-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="30851-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30851-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30851-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="30851-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30851-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="30851-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30851-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30851-135">DLL</span><span class="sxs-lookup"><span data-stu-id="30851-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30851-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30851-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30851-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="30851-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30851-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="30851-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="30851-139">**IWSManSession:: identificar**</span><span class="sxs-lookup"><span data-stu-id="30851-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="30851-140">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="30851-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





