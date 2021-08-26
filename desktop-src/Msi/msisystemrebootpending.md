---
description: O instalador definirá o valor da propriedade MsiSystemRebootPending como 1 se houver uma operação pendente para renomear um arquivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriedade MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cab600ca7c0f1bbc240f8fb1a9d93f3da62914e8250863333b75f8973d6c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042646"
---
# <a name="msisystemrebootpending-property"></a>Propriedade MsiSystemRebootPending

O instalador definirá o valor da propriedade **MsiSystemRebootPending** como 1 se houver uma operação pendente para renomear um arquivo.

Os autores de pacote podem basear uma condição na [tabela LaunchCondition](launchcondition-table.md) nessa propriedade para evitar a instalação do pacote nos casos em que há uma operação pendente para renomear um arquivo. Isso pode ser feito para evitar uma reinicialização do sistema operacional causado pela renomeação do arquivo. O instalador não define a propriedade **MsiSystemRebootPending** em todos os casos que exijam uma reinicialização do sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




