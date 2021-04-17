---
description: O objeto SummaryInfo é usado para ler, criar e atualizar propriedades de documento do fluxo de informações resumidas de um objeto de armazenamento.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Objeto SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747736"
---
# <a name="summaryinfo-object"></a>Objeto SummaryInfo

O objeto **SummaryInfo** é usado para ler, criar e atualizar propriedades de documento do [fluxo de informações resumidas](summary-information-stream.md) de um objeto de armazenamento.

## <a name="members"></a>Membros

O objeto **SummaryInfo** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SummaryInfo** tem esses métodos.



| Método                                 | Descrição                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mantenha**](summaryinfo-persist.md) | Formata e grava as propriedades armazenadas anteriormente no fluxo de [informações de resumo](summary-information-stream.md)padrão.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SummaryInfo** tem essas propriedades.



| Propriedade                                                                             | Descrição                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Propriedade Property (objeto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Obtém ou define o valor da propriedade especificada no fluxo de informações de resumo.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica o número atual de valores de propriedade no objeto de informações de resumo.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade SummaryInformation (objeto Database)**](database-summaryinformation.md)
</dt> <dt>

[**Propriedade SummaryInformation (objeto do instalador)**](installer-summaryinformation.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




