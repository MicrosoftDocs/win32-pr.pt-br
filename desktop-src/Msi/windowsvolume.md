---
description: O instalador define a propriedade WindowsVolume como o volume da pasta do Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propriedade WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3e0632fa981e9ea511be5017d02411bb6bb18355187c818ac3cd6c39e4f670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989930"
---
# <a name="windowsvolume-property"></a>Propriedade WindowsVolume

O instalador define a **propriedade WindowsVolume** como o volume da pasta do Windows. A propriedade sempre termina com uma faixa invertida. Isso pode ser usado para definir o local padrão para o volume em que Windows pasta está, porque a propriedade [**ROOTDRIVE**](rootdrive.md) não é necessariamente igual a essa unidade.

## <a name="remarks"></a>Comentários

Não use a **propriedade WindowsVolume** na coluna Diretório da [tabela](directory-table.md) Diretório. A [**propriedade WindowsFolder**](windowsfolder.md) contém o caminho para a pasta Windows dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou no Windows XP Consulte os Requisitos de Run-Time do instalador do [Windows](windows-installer-portal.md) para obter informações sobre o Windows service pack mínimo exigido por uma versão do Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




