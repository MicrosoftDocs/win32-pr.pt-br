---
description: Os dispositivos portáteis do Windows (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parâmetros de comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765003"
---
# <a name="command-parameters"></a>Parâmetros de comando

Os dispositivos portáteis do Windows (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.




| **Propriedade**                                            | **VarType**     | **Descrição**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ informações comuns do \_ cliente da propriedade WPD \_**          | **VT \_ desconhecido** | Uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) que o driver usa para identificar o cliente.                                                             |
| **\_contexto de \_ informações comuns do \_ cliente da \_ Propriedade WPD \_** | **LPWStr do VT \_**  | Um contexto especificado pelo driver que identifica um cliente para todas as operações subsequentes.                                                                                          |
| **\_categoria de \_ \_ comando comum de propriedade \_ WPD**            | **CLSID do VT \_**   | A parte **GUID** do valor **PROPERTYKEY** do comando.                                                                                                            |
| **\_ID de \_ \_ comando comum da propriedade \_ WPD**                  | **\_UI4 VT**     | A porção de ID exclusiva persistente (PID) do valor **PROPERTYKEY** do comando.                                                                                          |
| **\_destino de \_ \_ comando comum de propriedade \_ WPD**              | **LPWStr do VT \_**  | O identificador de objeto de destino.                                                                                                                                                |
| **\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**          | **\_UI4 VT**     | Um código de erro específico do driver retornado por um driver WPD.                                                                                                                       |
| **\_ \_ HRESULT comum de propriedade WPD \_**                      | **erro de VT \_**   | O valor **HRESULT** retornado por um driver WPD para uma operação específica.                                                                                                   |
| **\_IDs de \_ \_ objeto comum de propriedade \_ WPD**                  | **VT \_ desconhecido** | Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de Variant Type **VT \_ LPWSTR** que contém uma lista de identificadores de objeto. |
| **as \_ \_ \_ \_ IDs exclusivas persistentes comuns da propriedade WPD \_**      | **VT \_ desconhecido** | Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de Variant Type **VT \_ LPWSTR** que contém uma lista de PIDs.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




