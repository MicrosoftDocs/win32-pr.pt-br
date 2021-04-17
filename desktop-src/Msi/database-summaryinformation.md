---
description: A propriedade SummaryInformation do objeto Database retorna um objeto SummaryInfo que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de resumo.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propriedade Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748596"
---
# <a name="databasesummaryinformation-property"></a>Propriedade Database. SummaryInformation

A propriedade **SummaryInformation** do objeto [**Database**](database-object.md) retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao [fluxo de informações de resumo](summary-information-stream.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valor da propriedade

O número máximo de propriedades a serem adicionadas ou modificadas. Esse parâmetro é necessário e usado para alocar memória de trabalho suficiente durante a geração de fluxo. Não é necessário armazenar esse número de propriedades. Um valor de zero deve ser usado se o banco de dados for aberto como somente leitura para impedir que o fluxo seja atualizado.

## <a name="remarks"></a>Comentários

Se um valor de *maxProperties* maior que 0 for usado para abrir um fluxo de informações de resumo existente, o método [**Persist**](summaryinfo-persist.md) deverá ser chamado antes de fechar o objeto. A falha ao fazer isso perderá as informações de fluxo existentes.

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




