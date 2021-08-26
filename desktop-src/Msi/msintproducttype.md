---
description: o instalador define a propriedade MsiNTProductType para Windows NT, Windows 2000 e sistemas operacionais posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriedade MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e4c5083e5d1f0195e2e8a8e0cc46213853cb5cf1431535afee7e5362ff5eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082816"
---
# <a name="msintproducttype-property"></a>Propriedade MsiNTProductType

o instalador define a propriedade **MsiNTProductType** para Windows NT, Windows 2000 e sistemas operacionais posteriores. essa propriedade indica o tipo de produto Windows.

para os sistemas operacionais Windows 2000 e posteriores, o instalador define os valores a seguir. Observe que os valores são os mesmos do campo **wProductType** da estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Valor | Significado                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional e posterior      |
| 2     | Windows controlador de domínio 2000 e posterior |
| 3     | Windows o servidor 2000 e posterior            |



 

para sistemas operacionais anteriores à Windows 2000, o instalador define os valores a seguir.



| Valor | Significado                      |
|-------|------------------------------|
| 1     | Windows NT Estação       |
| 2     | controlador de domínio Windows NT |
| 3     | Windows NT Servidor            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
