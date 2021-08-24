---
title: Interface IDeliveryOptimizationFile
description: Implemente a interface IDeliveryOptimizationFile para identificar o status de um arquivo específico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635736"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interface IDeliveryOptimizationFile

Implemente a interface **IDeliveryOptimizationFile** para identificar o status de um arquivo específico.

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationFile** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationFile** tem esses métodos.



| Método                                                 | Descrição                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**Getstats**](ideliveryoptimizationfile-getstats.md) | Retorna estatísticas de download e upload para um arquivo específico.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte      | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]                                   |
| Servidor mínimo com suporte      | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]                               |
| Cabeçalho                        | Deliveryoptimization.h                                                           |
| Idl                           | DeliveryOptimization.idl                                                         |
| Biblioteca                       | Dosvc.lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2 |
