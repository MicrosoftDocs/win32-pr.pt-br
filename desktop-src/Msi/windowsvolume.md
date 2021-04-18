---
description: O instalador define a propriedade WindowsVolume para o volume da pasta do Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propriedade WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750586"
---
# <a name="windowsvolume-property"></a>Propriedade WindowsVolume

O instalador define a propriedade **WindowsVolume** para o volume da pasta do Windows. A propriedade sempre termina com uma barra invertida. Isso pode ser usado para definir o local padrão para o volume em que a pasta do Windows está, porque a propriedade [**ROOTDRIVE**](rootdrive.md) não necessariamente é igual a essa unidade.

## <a name="remarks"></a>Comentários

Não use a propriedade **WindowsVolume** na coluna Directory da tabela [Directory](directory-table.md) . A propriedade [**WindowsFolder**](windowsfolder.md) contém o caminho para a pasta do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




