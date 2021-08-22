---
description: Defina a propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS como 1 na tabela de propriedades ou em uma linha de comando.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae30e142167e2d080fa4c74c046625338fbf92fd4476b0339d60f77e321ab54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943937"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS

Defina a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** como 1 na [tabela de propriedades](property-table.md) ou em uma linha de comando. Quando essa propriedade tiver sido definida como 1, o instalador determinará se os componentes em quaisquer patches substituídos estão se tornando redundantes. O instalador pode cancelar o registro e desinstalar componentes redundantes para evitar deixar por trás componentes órfãos no computador.

A definição dessa propriedade afeta os componentes em todos os patches que estão sendo substituídos. Para habilitar essa funcionalidade para componentes únicos, use o atributo **msidbComponentAttributesUninstallOnSupersedence** na [tabela de componentes](component-table.md).

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. versões anteriores a Windows Installer 4,5 ignoram a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,5 ou Windows Installer 4,5 no Windows Vista, Windows XP, Windows server 2003 e Windows server 2008. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




