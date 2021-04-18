---
description: O PRIMARYFOLDER é uma propriedade global que permite que o autor designe uma pasta principal para a instalação.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propriedade PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752031"
---
# <a name="primaryfolder-property"></a>Propriedade PRIMARYFOLDER

O **PRIMARYFOLDER** é uma propriedade global que permite que o autor designe uma pasta principal para a instalação. O valor dessa propriedade deve ser o nome da chave de um diretório que existe na [tabela de diretórios](directory-table.md).

O instalador usa o caminho resolvido da pasta principal para determinar qual volume usar ao definir os valores da propriedade [**PrimaryVolumePath**](primaryvolumepath.md) , da propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , da propriedade [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) e da propriedade [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) . O instalador fornece os valores dessas últimas Propriedades aos usuários na interface do usuário para ajudá-los a gerenciar o espaço em disco. Os autores de pacote normalmente podem selecionar a pasta maior que a pasta principal.

O valor dessa propriedade deve ser o nome da chave de um registro de diretório encontrado na [tabela de diretórios](directory-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




