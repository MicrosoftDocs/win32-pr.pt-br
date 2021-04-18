---
description: Defina a propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS como 1 na tabela de propriedades ou em uma linha de comando.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757385"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS

Defina a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** como 1 na [tabela de propriedades](property-table.md) ou em uma linha de comando. Quando essa propriedade tiver sido definida como 1, o instalador determinará se os componentes em quaisquer patches substituídos estão se tornando redundantes. O instalador pode cancelar o registro e desinstalar componentes redundantes para evitar deixar por trás componentes órfãos no computador.

A definição dessa propriedade afeta os componentes em todos os patches que estão sendo substituídos. Para habilitar essa funcionalidade para componentes únicos, use o atributo **msidbComponentAttributesUninstallOnSupersedence** na [tabela de componentes](component-table.md).

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. Versões anteriores a Windows Installer 4,5 ignoram a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,5 ou Windows Installer 4,5 no Windows Vista, no Windows XP, no Windows Server 2003 e no Windows Server 2008. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




