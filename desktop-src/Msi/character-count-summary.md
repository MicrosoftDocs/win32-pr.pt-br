---
description: A propriedade de resumo contagem de caracteres só é usada em transformações.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propriedade de resumo contagem de caracteres
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766cc9ab355e533c155bfc81bac7b3f6e82cf9ab8679cf4feb00e9d01705a94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754336"
---
# <a name="character-count-summary-property"></a>Propriedade de resumo contagem de caracteres

A propriedade de **Resumo contagem de caracteres** só é usada em transformações. Essa parte do fluxo de informações de resumo é dividida em palavras de 2 16 bits. A palavra superior contém os [*sinalizadores de validação de transformação*](t-gly.md). A palavra inferior contém os [*sinalizadores de condição de erro de transformação*](t-gly.md).

Essa propriedade deve ser nula em um pacote de instalação ou em um pacote de patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




