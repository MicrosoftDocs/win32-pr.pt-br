---
description: O instalador define a propriedade MsiNTProductType para sistemas operacionais Windows NT, Windows 2000 e posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriedade MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758953"
---
# <a name="msintproducttype-property"></a>Propriedade MsiNTProductType

O instalador define a propriedade **MsiNTProductType** para sistemas operacionais Windows NT, Windows 2000 e posteriores. Essa propriedade indica o tipo de produto do Windows.

Para sistemas operacionais Windows 2000 e posteriores, o instalador define os valores a seguir. Observe que os valores são os mesmos do campo **wProductType** da estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Valor | Significado                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional e posterior      |
| 2     | Controlador de domínio do Windows 2000 e posterior |
| 3     | Windows 2000 Server e posterior            |



 

Para sistemas operacionais anteriores ao Windows 2000, o instalador define os valores a seguir.



| Valor | Significado                      |
|-------|------------------------------|
| 1     | Estação de trabalho do Windows NT       |
| 2     | Controlador de domínio do Windows NT |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
