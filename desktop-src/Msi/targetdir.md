---
description: A propriedade TARGETDIR especifica o diretório de destino raiz para a instalação.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propriedade TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759371"
---
# <a name="targetdir-property"></a>Propriedade TARGETDIR

A propriedade **TARGETDIR** especifica o diretório de destino raiz para a instalação. **TARGETDIR** deve ser o nome de uma raiz na tabela de [diretórios](directory-table.md) . Pode haver apenas um único diretório de destino raiz. Durante uma [instalação administrativa](administrative-installation.md) , essa propriedade especifica o local para copiar o pacote de instalação. Durante uma instalação não administrativa, essa propriedade especifica o diretório de destino raiz.

Para especificar o diretório de destino raiz, defina a coluna Directory da tabela Directory como a propriedade **TARGETDIR** e a coluna DefaultDir como a propriedade [**SourceDir**](sourcedir.md) . Se a propriedade **TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade. Se a propriedade **TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho. Para obter mais informações sobre como usar a propriedade **TARGETDIR** , consulte [usando a tabela de diretórios](using-the-directory-table.md).

Observe que o valor da propriedade **TARGETDIR** normalmente é definido na linha de comando ou por meio de uma interface do usuário. A definição de **TARGETDIR** por meio da criação de um caminho na [tabela de propriedades](property-table.md) não é recomendada porque os computadores diferem na configuração da unidade local.

Para obter mais informações sobre como alterar TARGETDIR durante uma instalação, consulte [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




