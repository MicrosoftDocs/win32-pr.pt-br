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
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764247"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interface IDeliveryOptimizationFile

Implemente a interface **IDeliveryOptimizationFile** para identificar o status de um arquivo específico.

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationFile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationFile** tem esses métodos.



| Método                                                 | Descrição                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Retorna o download e o upload de estatísticas para um arquivo específico.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte      | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]                                   |
| Servidor mínimo com suporte      | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]                               |
| parâmetro                        | Deliveryoptimization. h                                                           |
| INSERI                           | DeliveryOptimization. idl                                                         |
| Biblioteca                       | Dosvc. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2 |
