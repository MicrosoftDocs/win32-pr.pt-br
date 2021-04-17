---
description: O instalador definirá o valor da propriedade MsiSystemRebootPending como 1 se houver uma operação pendente para renomear um arquivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriedade MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759649"
---
# <a name="msisystemrebootpending-property"></a>Propriedade MsiSystemRebootPending

O instalador definirá o valor da propriedade **MsiSystemRebootPending** como 1 se houver uma operação pendente para renomear um arquivo.

Os autores de pacote podem basear uma condição na [tabela LaunchCondition](launchcondition-table.md) nessa propriedade para evitar a instalação do pacote nos casos em que há uma operação pendente para renomear um arquivo. Isso pode ser feito para evitar uma reinicialização do sistema operacional causado pela renomeação do arquivo. O instalador não define a propriedade **MsiSystemRebootPending** em todos os casos que exijam uma reinicialização do sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 4,5 no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




