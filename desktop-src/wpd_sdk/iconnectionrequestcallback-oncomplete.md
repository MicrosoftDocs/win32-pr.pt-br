---
description: Notifica um aplicativo de que uma solicitação de conexão ou desconexão agendada anteriormente para o dispositivo MTP/Bluetooth foi concluída.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Método IConnectionRequestCallback:: OnComplete (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829091"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="9405c-103">Método IConnectionRequestCallback:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="9405c-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="9405c-104">O método **OnComplete** notifica um aplicativo de que uma solicitação de conexão ou desconexão agendada anteriormente para o dispositivo MTP/Bluetooth foi concluída</span><span class="sxs-lookup"><span data-stu-id="9405c-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="9405c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9405c-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="9405c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9405c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9405c-107">*hrStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9405c-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9405c-108">O status da solicitação para conectar ou desconectar um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9405c-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9405c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9405c-109">Return value</span></span>

<span data-ttu-id="9405c-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9405c-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9405c-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9405c-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9405c-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9405c-112">Return code</span></span>                                                                          | <span data-ttu-id="9405c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="9405c-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9405c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9405c-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9405c-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9405c-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9405c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9405c-116">Remarks</span></span>

<span data-ttu-id="9405c-117">Um aplicativo implementa a interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para receber notificações sobre solicitações concluídas e para cancelar solicitações pendentes.</span><span class="sxs-lookup"><span data-stu-id="9405c-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="9405c-118">Os dispositivos portáteis do Windows (WPD) chamam esse método para notificar um aplicativo de que uma solicitação agendada anteriormente foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9405c-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="9405c-119">Cada solicitação pode ser rastreada e cancelada por seu retorno de chamada fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9405c-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="9405c-120">Portanto, se o aplicativo precisar enviar várias solicitações ao mesmo tempo usando o mesmo objeto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , cada solicitação deverá passar um objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) exclusivo como o parâmetro de entrada para os métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="9405c-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="9405c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9405c-121">Requirements</span></span>



| <span data-ttu-id="9405c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9405c-122">Requirement</span></span> | <span data-ttu-id="9405c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9405c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9405c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9405c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9405c-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9405c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="9405c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9405c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9405c-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9405c-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="9405c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9405c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9405c-129"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9405c-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="9405c-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="9405c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9405c-131"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9405c-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="9405c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9405c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9405c-133"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9405c-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="9405c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9405c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9405c-135">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="9405c-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




