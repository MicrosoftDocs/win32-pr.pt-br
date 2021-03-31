---
description: Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Método IUpdateEndpointAuthProvider:: GetEndpointToken (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647294"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="ccffd-103">Método IUpdateEndpointAuthProvider:: GetEndpointToken</span><span class="sxs-lookup"><span data-stu-id="ccffd-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="ccffd-104">Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.</span><span class="sxs-lookup"><span data-stu-id="ccffd-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccffd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccffd-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="ccffd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccffd-107">*ServiceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-108">Identifica o serviço a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ccffd-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="ccffd-109">*ponto de extremidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-110">Identifica o tipo de ponto de extremidade que é implementado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="ccffd-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="ccffd-111">*proxySettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-112">As configurações a serem usadas ao se conectar a um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="ccffd-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="ccffd-113">Consulte a estrutura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="ccffd-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="ccffd-114">*hUserToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="ccffd-115">*TokenType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-116">Identifica o tipo de token de autenticação que é usado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="ccffd-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ccffd-117">*fRefreshOnline* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-118">Indica que o WUA do clima solicita um novo token.</span><span class="sxs-lookup"><span data-stu-id="ccffd-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="ccffd-119">Verdadeiro indica que um novo token é solicitado.</span><span class="sxs-lookup"><span data-stu-id="ccffd-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="ccffd-120">False indica que um token novo ou armazenado em cache é solicitado.</span><span class="sxs-lookup"><span data-stu-id="ccffd-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="ccffd-121">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ccffd-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="ccffd-122">*ppEndpointToken* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccffd-123">Especifique o token do ponto de extremidade a ser usado.</span><span class="sxs-lookup"><span data-stu-id="ccffd-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccffd-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccffd-124">Return value</span></span>

<span data-ttu-id="ccffd-125">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ccffd-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="ccffd-126">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="ccffd-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccffd-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccffd-127">Remarks</span></span>

<span data-ttu-id="ccffd-128">O WUA normalmente define o parâmetro fRefreshOnline como false quando esse método é chamado pela primeira vez; em seguida, se um erro de conexão ocorrer, o WUA definirá esse parâmetro como true quando o método for chamado novamente.</span><span class="sxs-lookup"><span data-stu-id="ccffd-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="ccffd-129">No entanto, a implementação desse método pode solicitar um novo token de um serviço de token de segurança (STS) ou fornecer um token em cache a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="ccffd-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccffd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccffd-130">Requirements</span></span>



| <span data-ttu-id="ccffd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccffd-131">Requirement</span></span> | <span data-ttu-id="ccffd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ccffd-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccffd-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccffd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ccffd-134">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="ccffd-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccffd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ccffd-136">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="ccffd-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ccffd-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccffd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccffd-138"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccffd-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccffd-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="ccffd-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccffd-140"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccffd-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="ccffd-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccffd-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="ccffd-142"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccffd-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="ccffd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ccffd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccffd-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccffd-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccffd-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccffd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccffd-146">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="ccffd-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




