---
description: A propriedade VerifyDiskSpace é uma propriedade somente leitura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Propriedade Session. VerifyDiskSpace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768718"
---
# <a name="sessionverifydiskspace-property"></a>Propriedade Session. VerifyDiskSpace

A propriedade **VerifyDiskSpace** é uma propriedade somente leitura. Retornará true se houver espaço em disco suficiente e false se o disco estiver cheio. Como essa propriedade usa as informações coletadas pelas ações de custo, **VerifyDiskSpace** deve ser chamado somente após a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




