---
description: Para um pacote de instalação, a propriedade Resumo do número de revisão contém o código do pacote do instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propriedade de resumo do número de revisão
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11371c4a431322fd7ceca7fd645fc8eb8bea47688b740340e973507271f6a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869056"
---
# <a name="revision-number-summary-property"></a>Propriedade de resumo do número de revisão

Para um pacote de instalação, a propriedade **Resumo do número de revisão** contém o código do [*pacote*](p-gly.md) do instalador. Para obter mais informações sobre códigos de pacote, consulte [Package codes](package-codes.md).

Para uma transformação, a propriedade **Resumo do número de revisão** lista os GUIDs de código do produto e a versão dos produtos novos e originais e o GUID do código de atualização. A lista é separada com ponto e vírgula da seguinte maneira.

"Original-produto-código original-versão do produto; Código de New-Product novo – versão do produto; Atualizar código "

Para um pacote de patch, a propriedade **Resumo do número de revisão** especifica o código de patch GUID para o patch. Isso pode ser seguido por uma lista de GUIDs de código de patch para patches obsoletos que devem ser removidos quando esse patch é aplicado. Os códigos de patch são concatenados sem delimitadores separando GUIDs na lista.

* * Windows Installer 3,0: * * se houver informações de sequenciamento presentes na [tabela MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 usará as informações de sequenciamento na tabela e ignorará a lista de patches obsoletos incluídos na propriedade **resumo do número de revisão** . Windows O instalador 3,0 ainda pode usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.

* * Windows Installer 2,0: * * não há suporte para a [tabela MsiPatchSequence](msipatchsequence-table.md) . Windows O instalador 2,0 ainda pode usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.

Essa propriedade de resumo é necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




