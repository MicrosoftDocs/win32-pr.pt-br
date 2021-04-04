---
title: Interface IDeliveryOptimizationJob (Deliveryoptimization. h)
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
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085547"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interface IDeliveryOptimizationJob

Use a interface **IDeliveryOptimizationJob** para baixar intervalos de um arquivo.

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationJob** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationJob** tem esses métodos.



| Método                                                                  | Descrição                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

