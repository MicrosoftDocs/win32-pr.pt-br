---
description: A propriedade Resumo de comentários transmite a finalidade geral do pacote de instalação, da transformação ou do pacote de patch.
ms.assetid: e9034bfb-1b32-4851-ac23-4c3223760a04
title: Propriedade de Resumo de comentários
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351023eddb057a47bf5cfc67b7ef869d905eb126
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768478"
---
# <a name="comments-summary-property"></a>Propriedade de Resumo de comentários

A propriedade **Resumo de comentários** transmite a finalidade geral do pacote de instalação, da transformação ou do pacote de patch.

Um autor de um pacote de instalação, transformação ou pacote de patch deve definir o valor da propriedade **Resumo de comentários** como um dos seguintes valores:

<dl> "Este banco de dados do instalador contém a lógica e os requisitos necessários para instalar <> do *produto* ".  
"Essa transformação contém a lógica e os dados necessários para instalar <> do *produto* ".  
"Este patch contém a lógica e os dados necessários para instalar <> do *produto* ".  
</dl>

em que <*produto*> é o nome do produto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




