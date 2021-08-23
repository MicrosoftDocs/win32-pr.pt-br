---
description: A propriedade TARGETDIR especifica o diretório de destino raiz para a instalação.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propriedade TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b61575de21b47b1d82764d96e5876a9fd4c89fb1f837150988aa2c7a08e07be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626596"
---
# <a name="targetdir-property"></a>Propriedade TARGETDIR

A propriedade **TARGETDIR** especifica o diretório de destino raiz para a instalação. **TARGETDIR** deve ser o nome de uma raiz na tabela de [diretórios](directory-table.md) . Pode haver apenas um único diretório de destino raiz. Durante uma [instalação administrativa](administrative-installation.md) , essa propriedade especifica o local para copiar o pacote de instalação. Durante uma instalação não administrativa, essa propriedade especifica o diretório de destino raiz.

Para especificar o diretório de destino raiz, defina a coluna Directory da tabela Directory como a propriedade **TARGETDIR** e a coluna DefaultDir como a propriedade [**SourceDir**](sourcedir.md) . Se a propriedade **TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade. Se a propriedade **TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho. Para obter mais informações sobre como usar a propriedade **TARGETDIR** , consulte [usando a tabela de diretórios](using-the-directory-table.md).

Observe que o valor da propriedade **TARGETDIR** normalmente é definido na linha de comando ou por meio de uma interface do usuário. A definição de **TARGETDIR** por meio da criação de um caminho na [tabela de propriedades](property-table.md) não é recomendada porque os computadores diferem na configuração da unidade local.

Para obter mais informações sobre como alterar TARGETDIR durante uma instalação, consulte [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




