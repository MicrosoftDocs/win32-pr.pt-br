---
description: Solicita um ponto de extremidade que é usado para se conectar a um serviço.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Método IUpdateEndpointProvider:: getserviceendpoint (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767807"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="432bc-103">Método IUpdateEndpointProvider:: getserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="432bc-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="432bc-104">Solicita um ponto de extremidade que é usado para se conectar a um serviço.</span><span class="sxs-lookup"><span data-stu-id="432bc-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="432bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="432bc-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="432bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="432bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="432bc-107">*ServiceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="432bc-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-108">Identifica o serviço a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="432bc-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="432bc-109">*ponto de extremidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="432bc-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-110">Identifica o tipo de ponto de extremidade implementado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="432bc-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="432bc-111">A enumeração [**UpdateEndpointType**](updateendpointtype.md) define as constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="432bc-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="432bc-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="432bc-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="432bc-113">Um ponto de extremidade cliente-servidor usado para se conectar ao serviço de atualização.</span><span class="sxs-lookup"><span data-stu-id="432bc-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="432bc-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="432bc-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="432bc-115">Um ponto de extremidade de relatório usado quando o cliente relata os resultados de verificações, downloads e instalações de volta para o serviço de atualização</span><span class="sxs-lookup"><span data-stu-id="432bc-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="432bc-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="432bc-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="432bc-117">Um ponto de extremidade Self-Update que é usado quando o computador cliente entra em contato com um serviço de atualização para ver se há uma nova versão do software cliente do Windows Update Agent.</span><span class="sxs-lookup"><span data-stu-id="432bc-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="432bc-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="432bc-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="432bc-119">Um ponto de extremidade de regulamentação que é usado quando o computador cliente entra em contato com o serviço regulamento para agir em uma atualização específica aplicável ao computador de destino.</span><span class="sxs-lookup"><span data-stu-id="432bc-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="432bc-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="432bc-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="432bc-121">Um Simple-Targeting endoint que é usado somente com serviços privados (servidores WSUS em ambientes corporativos).</span><span class="sxs-lookup"><span data-stu-id="432bc-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="432bc-122">*proxySettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="432bc-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-123">Identifica as configurações que são usadas ao se conectar a um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="432bc-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="432bc-124">*hUserToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="432bc-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-125">Contém um objeto identificador de token que representa o usuário.</span><span class="sxs-lookup"><span data-stu-id="432bc-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="432bc-126">O provedor de ponto de extremidade usa esse token para determinar quais configurações de proxy e credenciais usar.</span><span class="sxs-lookup"><span data-stu-id="432bc-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="432bc-127">*fRefreshOnline* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="432bc-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-128">Indica que o WUA do clima solicita um novo token.</span><span class="sxs-lookup"><span data-stu-id="432bc-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="432bc-129">Verdadeiro indica que um novo token é solicitado.</span><span class="sxs-lookup"><span data-stu-id="432bc-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="432bc-130">False indica que um token novo ou armazenado em cache é solicitado.</span><span class="sxs-lookup"><span data-stu-id="432bc-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="432bc-131">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="432bc-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="432bc-132">*pbstrEndpointLoc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="432bc-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="432bc-133">Especifique a URL usada para se comunicar com o serviço.</span><span class="sxs-lookup"><span data-stu-id="432bc-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="432bc-134">Por exemplo, para um ponto de extremidade cleint-Server, essa seria a URL para o serviço do servidor cliente.</span><span class="sxs-lookup"><span data-stu-id="432bc-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="432bc-135">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="432bc-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="432bc-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="432bc-136">Return value</span></span>

<span data-ttu-id="432bc-137">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="432bc-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="432bc-138">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="432bc-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="432bc-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="432bc-139">Remarks</span></span>

<span data-ttu-id="432bc-140">O WUA normalmente define o parâmetro *fRefreshOnline* como false quando esse método é chamado pela primeira vez; em seguida, se um erro de conexão ocorrer, o WUA definirá esse parâmetro como true quando o método for chamado novamente.</span><span class="sxs-lookup"><span data-stu-id="432bc-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="432bc-141">No entanto, a implementação desse método pode solicitar um novo token de um serviço de token de segurança (STS) ou fornecer um token em cache a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="432bc-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="432bc-142">Se o ponto de extremidade não precisar de autenticação, o chamador poderá se conectar ao serviço usando apenas a URL especificada pelo parâmetro *pbstrEndpointLoc* .</span><span class="sxs-lookup"><span data-stu-id="432bc-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="432bc-143">Se o ponto de extremidade precisar de autenticação, o chamador poderá usar a URL especificada pelo parâmetro *pbstrEndpointLoc* e os dados fornecidos pelos outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="432bc-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="432bc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="432bc-144">Requirements</span></span>



| <span data-ttu-id="432bc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="432bc-145">Requirement</span></span> | <span data-ttu-id="432bc-146">Valor</span><span class="sxs-lookup"><span data-stu-id="432bc-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="432bc-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="432bc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="432bc-148">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="432bc-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="432bc-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="432bc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="432bc-150">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="432bc-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="432bc-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="432bc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="432bc-152"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="432bc-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="432bc-153">INSERI</span><span class="sxs-lookup"><span data-stu-id="432bc-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="432bc-154"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="432bc-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="432bc-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="432bc-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="432bc-156"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="432bc-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="432bc-157">DLL</span><span class="sxs-lookup"><span data-stu-id="432bc-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="432bc-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="432bc-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="432bc-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="432bc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="432bc-160">**IUpdateEndpointProvider**</span><span class="sxs-lookup"><span data-stu-id="432bc-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




