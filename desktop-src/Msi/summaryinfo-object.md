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
ms.openlocfilehash: 3efdc009f40f0bce67559d185afb4cba1289c00fc1d7771a43d392601220dbae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039586"
---
# <a name="summaryinfo-object"></a>Objeto SummaryInfo

O **objeto SummaryInfo** é usado para ler, criar e atualizar propriedades de documento do fluxo de informações [resumidas](summary-information-stream.md) de um objeto de armazenamento.

## <a name="members"></a>Membros

O **objeto SummaryInfo** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto SummaryInfo** tem esses métodos.



| Método                                 | Descrição                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Persistir**](summaryinfo-persist.md) | Formatar e grava as propriedades armazenadas anteriormente no fluxo de informações [de resumo padrão.](summary-information-stream.md)<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto SummaryInfo** tem essas propriedades.



| Propriedade                                                                             | Descrição                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Propriedade Property (objeto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Obtém ou define o valor da propriedade especificada no fluxo de informações de resumo.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica o número atual de valores de propriedade no objeto de informações de resumo.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISummaryInfo é definido como \_ 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedade SummaryInformation (objeto database)**](database-summaryinformation.md)
</dt> <dt>

[**Propriedade SummaryInformation (objeto installer)**](installer-summaryinformation.md)
</dt> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




