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
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751647"
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
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




