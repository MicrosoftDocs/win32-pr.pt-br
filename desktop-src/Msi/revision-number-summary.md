---
description: Para um pacote de instalação, a propriedade Resumo do número de revisão contém o código do pacote do instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propriedade de resumo do número de revisão
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747739"
---
# <a name="revision-number-summary-property"></a>Propriedade de resumo do número de revisão

Para um pacote de instalação, a propriedade **Resumo do número de revisão** contém o código do [*pacote*](p-gly.md) do instalador. Para obter mais informações sobre códigos de pacote, consulte [Package codes](package-codes.md).

Para uma transformação, a propriedade **Resumo do número de revisão** lista os GUIDs de código do produto e a versão dos produtos novos e originais e o GUID do código de atualização. A lista é separada com ponto e vírgula da seguinte maneira.

"Original-produto-código original-versão do produto; Código de New-Product novo – versão do produto; Atualizar código "

Para um pacote de patch, a propriedade **Resumo do número de revisão** especifica o código de patch GUID para o patch. Isso pode ser seguido por uma lista de GUIDs de código de patch para patches obsoletos que devem ser removidos quando esse patch é aplicado. Os códigos de patch são concatenados sem delimitadores separando GUIDs na lista.

* * Windows Installer 3,0: * * se houver informações de sequenciamento presentes na [tabela MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 usará as informações de sequenciamento na tabela e ignorará a lista de patches obsoletos incluídos na propriedade **Resumo do número de revisão** . Windows Installer 3,0 ainda poderá usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.

* * Windows Installer 2,0: * * não há suporte para a [tabela MsiPatchSequence](msipatchsequence-table.md) . Windows Installer 2,0 ainda poderá usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.

Essa propriedade de resumo é necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




