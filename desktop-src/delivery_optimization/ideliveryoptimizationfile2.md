---
title: Interface IDeliveryOptimizationFile2
description: O IDeliveryOptimizationFile2 dá suporte à configuração e à obter propriedades de arquivo opcionais.
keywords:
- Interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7409635444885b662688ce94c300aae6e62186dd76bd7278b3e7445ef50c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542041"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interface IDeliveryOptimizationFile2

O **IDeliveryOptimizationFile2** dá suporte à configuração e à obter propriedades de arquivo opcionais. 

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationFile2** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile2** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationFile2** tem esses métodos.

| Método                                                 | Descrição                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**Getproperty**](ideliveryoptimizationfile2-getproperty.md)  | Esse método retorna uma única propriedade do arquivo DO. |
| [**Setproperty**](ideliveryoptimizationfile2-setproperty.md)  | Esse método define uma única propriedade do arquivo DO.    |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte      | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]                                    |
| Servidor mínimo com suporte      | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]                                |
| Cabeçalho                        | Deliveryoptimization.h                                                            |
| Idl                           | DeliveryOptimization.idl                                                          |
| Biblioteca                       | Dosvc.lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 é definido como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
