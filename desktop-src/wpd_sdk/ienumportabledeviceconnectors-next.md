---
description: Recupera um ou mais objetos IPortableDeviceConnector na sequência de enumeração.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: Método IEnumPortableDeviceConnectors::Next (Devpkey.h)
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
ms.openlocfilehash: 868f13f220dbd5d5867e5ee2bbb54c1ef946e267d87e9ea0aa625108b945d537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697291"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a>Método IEnumPortableDeviceConnectors::Next

O **método Next** recupera os próximos objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cRequested* \[ Em\]
</dt> <dd>

O número de dispositivos solicitados. Esse valor também indica o número de elementos na matriz alocada pelo chamador especificada pelo *parâmetro pConnectors.*

</dd> <dt>

*pConnectors* \[ out\]
</dt> <dd>

Uma matriz de [**ponteiros IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) cada um especificando um dispositivo MTP Bluetooth emparelhado. O chamador deve alocar uma matriz de ponteiros **IPortableDeviceConnector,** com o comprimento da matriz especificado pelo *parâmetro cRequested.* No retorno bem-sucedido, o chamador deve liberar a matriz e os ponteiros retornados. As interfaces **IPortableDeviceConnector** são liberadas chamando o **método IUnknown::Release.**

</dd> <dt>

*pcFetched* \[ in, out\]
</dt> <dd>

O número de [**interfaces IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) que realmente são recuperadas. Se nenhuma interface **IPortableDeviceConnector** for recuperada e o valor de retorno for **S \_ FALSE,** não haverá mais interfaces **IPortableDeviceConnector** a enumerar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O método foi bem-sucedido.<br/>                                 |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Não há mais dispositivos MTP Bluetooth para enumerar.<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso desse método para enumerar dispositivos MTP/Bluetooth emparelhados e enviar uma solicitação de conexão assíncrona para cada um.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| parâmetro<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




