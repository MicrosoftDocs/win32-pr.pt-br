---
description: 'Libera os identificadores de plug and Play (PnP) que são recuperados pelos métodos IPortableDeviceManager:: Devices ou IPortableDeviceServiceManager:: getdeviceservices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Função FreePortableDevicePnPIDs (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170687"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="69c8f-103">Função FreePortableDevicePnPIDs</span><span class="sxs-lookup"><span data-stu-id="69c8f-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="69c8f-104">A função auxiliar **FreePortableDevicePnPIDs** libera os identificadores de plug and Play (PnP) que são recuperados pelos métodos [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ou [**IPortableDeviceServiceManager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="69c8f-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69c8f-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="69c8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69c8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c8f-107">*pPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="69c8f-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="69c8f-108">A matriz de identificadores de Plug and Play (PnP) a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="69c8f-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="69c8f-109">*cPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="69c8f-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="69c8f-110">O número de identificadores na matriz especificada pelo parâmetro *pPnPIDs* .</span><span class="sxs-lookup"><span data-stu-id="69c8f-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c8f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69c8f-111">Return value</span></span>

<span data-ttu-id="69c8f-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="69c8f-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c8f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="69c8f-113">Remarks</span></span>

<span data-ttu-id="69c8f-114">O aplicativo é responsável por liberar a matriz de ponteiros que ela aloca.</span><span class="sxs-lookup"><span data-stu-id="69c8f-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="69c8f-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69c8f-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="69c8f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c8f-116">Requirements</span></span>



| <span data-ttu-id="69c8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c8f-117">Requirement</span></span> | <span data-ttu-id="69c8f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="69c8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c8f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69c8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69c8f-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69c8f-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="69c8f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69c8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69c8f-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="69c8f-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="69c8f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69c8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c8f-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c8f-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




