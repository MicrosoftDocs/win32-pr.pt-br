---
title: Interface IDeliveryOptimizationFile2
description: O IDeliveryOptimizationFile2 dá suporte à configuração e à obtenção de propriedades de arquivo opcionais.
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
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009137"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interface IDeliveryOptimizationFile2

O **IDeliveryOptimizationFile2** dá suporte à configuração e à obtenção de propriedades de arquivo opcionais. 

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationFile2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile2** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationFile2** tem esses métodos.

| Método                                                 | Descrição                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Esse método retorna uma única propriedade do arquivo do. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Esse método define uma única propriedade do arquivo do.    |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte      | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]                                    |
| Servidor mínimo com suporte      | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]                                |
| parâmetro                        | Deliveryoptimization. h                                                            |
| INSERI                           | DeliveryOptimization. idl                                                          |
| Biblioteca                       | Dosvc. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 é definido como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
