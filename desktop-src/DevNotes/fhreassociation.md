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
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756408"
---
# <a name="fhreassociation-class"></a>Classe FhReassociation

Representa o recurso de reassociação de histórico de arquivo, que permite que um usuário restabeleça uma relação com um destino de backup que foi usado pelo mesmo usuário no passado. A reassociação é executada chamando os métodos da interface [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Quando implementar

A API de histórico de arquivo implementa essa classe. Para criar uma instância dessa classe, use a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
