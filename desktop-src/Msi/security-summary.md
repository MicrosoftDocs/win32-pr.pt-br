---
description: A propriedade Resumo de segurança transmite se o pacote deve ser aberto como somente leitura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propriedade de Resumo de segurança
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750218"
---
# <a name="security-summary-property"></a>Propriedade de Resumo de segurança

A propriedade **Resumo de segurança** transmite se o pacote deve ser aberto como somente leitura. A ferramenta de edição de banco de dados não deve modificar um banco de dados imposto somente leitura e emitir um aviso em tentativas de modificar um banco de dados recomendado somente leitura. Os seguintes valores dessa propriedade são aplicáveis a Windows Installer arquivos.



| Valor | Descrição           |
|-------|-----------------------|
| 0     | Nenhuma restrição        |
| 2     | Somente leitura recomendado |
| 4     | Imposto somente leitura    |



 

Essa propriedade deve ser definida como somente leitura recomendado (2) para um banco de dados de instalação e para somente leitura (4) para uma transformação ou patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




