---
title: Interface IDeliveryOptimizationJob2
description: 'Saiba mais sobre: interface IDeliveryOptimizationJob2'
keywords:
- Interface IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764209"
---
# <a name="ideliveryoptimizationjob2-interface"></a>Interface IDeliveryOptimizationJob2

O IDeliveryOptimizationJob2 permite adicionar um único arquivo ao trabalho de download e recuperar o arquivo imediatamente. Essa interface também dá suporte à configuração e à obtenção de propriedades de trabalho opcionais.

## <a name="members"></a>Membros

A interface **IDeliveryOptimizationJob2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob2** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDeliveryOptimizationJob2** tem esses métodos.

| Método                                              | Descrição                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | O método AddFile adiciona um único arquivo a um trabalho existente DO.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | O método AddFile adiciona um único arquivo a um trabalho existente DO. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Este método não é usado.                                       |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]                                   |
| Servidor mínimo com suporte | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]                               |
| parâmetro                   | Deliveryoptimization. h                                                           |
| INSERI                      | DeliveryOptimization. idl                                                         |
| Biblioteca                  | Dosvc. lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
