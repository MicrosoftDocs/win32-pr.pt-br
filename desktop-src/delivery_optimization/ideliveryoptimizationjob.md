---
title: Interface IDeliveryOptimizationJob (Deliveryoptimization.h)
description: Use a interface IDeliveryOptimizationJob para baixar intervalos de um arquivo.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71f978be993e21ad487af5469327b5f66804166a7e5247dffb841f7815b2279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895676"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interface IDeliveryOptimizationJob

Use a interface **IDeliveryOptimizationJob** para baixar intervalos de um arquivo.

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationJob** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationJob** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationJob** tem esses métodos.



| Método                                                                  | Descrição                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

