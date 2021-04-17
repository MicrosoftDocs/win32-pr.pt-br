---
description: A propriedade MSIFASTINSTALL pode ser usada para reduzir o tempo necessário para instalar um grande pacote de Windows Installer.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propriedade MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748766"
---
# <a name="msifastinstall-property"></a>Propriedade MSIFASTINSTALL

A propriedade **MSIFASTINSTALL** pode ser usada para reduzir o tempo necessário para instalar um grande pacote de Windows Installer. A propriedade pode ser definida na linha de comando ou na tabela de [Propriedades](property-table.md) para configurar as operações que o usuário ou o desenvolvedor determina não são essenciais para a instalação.

O valor da propriedade **MSIFASTINSTALL** pode ser uma combinação dos valores a seguir.



| Valor | Significado                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valor padrão                                                                |
| 1     | Nenhum ponto de restauração do sistema foi salvo para esta instalação.                      |
| 2     | Execute apenas o [custo do arquivo](file-costing.md) e pule a verificação de outros custos. |
| 4     | Reduza a frequência das mensagens de progresso.                                   |



 

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Essa propriedade está disponível a partir do Windows Installer 5,0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



 

 




