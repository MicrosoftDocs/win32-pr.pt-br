---
description: Recupera o próximo um ou mais objetos IPortableDeviceConnector na sequência de enumeração.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'Método IEnumPortableDeviceConnectors:: Next (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802069"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="ae3d5-103">Método IEnumPortableDeviceConnectors:: Next</span><span class="sxs-lookup"><span data-stu-id="ae3d5-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="ae3d5-104">O **próximo** método recupera o próximo um ou mais objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae3d5-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ae3d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae3d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae3d5-107">*cRequested* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae3d5-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d5-108">O número de dispositivos solicitados.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-108">The number of requested devices.</span></span> <span data-ttu-id="ae3d5-109">Esse valor também indica o número de elementos na matriz alocada pelo chamador especificada pelo parâmetro *pConnectors* .</span><span class="sxs-lookup"><span data-stu-id="ae3d5-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ae3d5-110">*pConnectors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ae3d5-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d5-111">Uma matriz de ponteiros [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , cada um especificando um dispositivo MTP Bluetooth emparelhado.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="ae3d5-112">O chamador deve alocar uma matriz de ponteiros **IPortableDeviceConnector** , com o comprimento da matriz especificado pelo parâmetro *cRequested* .</span><span class="sxs-lookup"><span data-stu-id="ae3d5-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="ae3d5-113">No retorno bem-sucedido, o chamador deve liberar a matriz e os ponteiros retornados.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="ae3d5-114">As interfaces **IPortableDeviceConnector** são liberadas chamando o método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="ae3d5-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="ae3d5-115">*pcFetched* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ae3d5-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d5-116">O número de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) que são realmente recuperadas.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="ae3d5-117">Se nenhuma interface **IPortableDeviceConnector** for recuperada e o valor de retorno for **S \_ false**, não haverá mais interfaces **IPortableDeviceConnector** para enumerar.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae3d5-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae3d5-118">Return value</span></span>

<span data-ttu-id="ae3d5-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ae3d5-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ae3d5-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ae3d5-121">Return code</span></span>                                                                             | <span data-ttu-id="ae3d5-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae3d5-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae3d5-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d5-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ae3d5-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="ae3d5-125"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d5-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ae3d5-126">Não há mais dispositivos Bluetooth MTP para enumerar.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="ae3d5-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae3d5-127">Examples</span></span>

<span data-ttu-id="ae3d5-128">O exemplo a seguir demonstra o uso desse método para enumerar dispositivos MTP/Bluetooth emparelhados e para enviar uma solicitação de conexão assíncrona para cada um.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="ae3d5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae3d5-129">Requirements</span></span>



| <span data-ttu-id="ae3d5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae3d5-130">Requirement</span></span> | <span data-ttu-id="ae3d5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ae3d5-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3d5-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3d5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3d5-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ae3d5-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="ae3d5-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3d5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3d5-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ae3d5-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="ae3d5-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae3d5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae3d5-137"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d5-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="ae3d5-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="ae3d5-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae3d5-139"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d5-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="ae3d5-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae3d5-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae3d5-141"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d5-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="ae3d5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae3d5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3d5-143">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="ae3d5-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




