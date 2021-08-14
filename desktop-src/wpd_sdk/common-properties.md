---
description: Windows Os dispositivos portáteis (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.
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
ms.openlocfilehash: e5c58652c27d62e2954e86b9170e2f0a2d4ae4021743ced769adbf46a1f082b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431053"
---
# <a name="command-parameters"></a>Parâmetros de comando

Windows Os dispositivos portáteis (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.




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

 

 




