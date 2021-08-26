---
description: A propriedade SummaryInformation do objeto do instalador retorna um objeto SummaryInfo que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de Resumo de um pacote ou transformação.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Propriedade Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f671a5424e1008787443a13f2b72e75cb931da2f0783681c360a1b03ad640aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043616"
---
# <a name="installersummaryinformation-property"></a>Propriedade Installer. SummaryInformation

A propriedade **SummaryInformation** do objeto do [**instalador**](installer-object.md) retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de Resumo de um pacote ou transformação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se um valor de *maxProperties* maior que 0 for usado para abrir um fluxo de informações de resumo existente, o método [**Persist**](summaryinfo-persist.md) deverá ser chamado antes de fechar o objeto. A falha de fazer isso perde as informações de fluxo existentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




