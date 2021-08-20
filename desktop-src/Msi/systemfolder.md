---
description: O instalador define a propriedade SystemFolder como o caminho completo da pasta Sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propriedade SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567942e981af161654d41988ef797b64116af5cdb25e07a3d4f1465fc4ce975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142004"
---
# <a name="systemfolder-property"></a>Propriedade SystemFolder

O instalador define a **propriedade SystemFolder** como o caminho completo da pasta Sistema.

## <a name="remarks"></a>Comentários

O instalador define essa propriedade. Por exemplo, em 32 bits Windows o valor pode ser C: \\ Windows \\ System32. No Windows de 64 bits, o valor pode ser C: \\ Windows \\ SysWow64.

Normalmente, essa pasta é um subdiretório da pasta Windows dados. No entanto, ele reside em um servidor quando configurado para o shared Windows.

Essa pasta é local, mesmo quando configurada para Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




