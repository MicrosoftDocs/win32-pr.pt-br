---
description: A propriedade de resumo contagem de caracteres só é usada em transformações.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propriedade de resumo contagem de caracteres
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756905"
---
# <a name="character-count-summary-property"></a>Propriedade de resumo contagem de caracteres

A propriedade de **Resumo contagem de caracteres** só é usada em transformações. Essa parte do fluxo de informações de resumo é dividida em palavras de 2 16 bits. A palavra superior contém os [*sinalizadores de validação de transformação*](t-gly.md). A palavra inferior contém os [*sinalizadores de condição de erro de transformação*](t-gly.md).

Essa propriedade deve ser nula em um pacote de instalação ou em um pacote de patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




