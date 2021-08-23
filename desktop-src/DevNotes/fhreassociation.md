---
description: Representa o recurso de reassociação de histórico de arquivo, que permite que um usuário restabeleça uma relação com um destino de backup que foi usado pelo mesmo usuário no passado. A reassociação é executada chamando os métodos da interface IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Classe FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: f4b8cb55ce4b374f7f17f16044811a930623fc777a028ee98b5d8726bf714cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538506"
---
# <a name="fhreassociation-class"></a>Classe FhReassociation

Representa o recurso de reassociação de histórico de arquivo, que permite que um usuário restabeleça uma relação com um destino de backup que foi usado pelo mesmo usuário no passado. A reassociação é executada chamando os métodos da interface [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Quando implementar

A API de histórico de arquivo implementa essa classe. Para criar uma instância dessa classe, use a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
