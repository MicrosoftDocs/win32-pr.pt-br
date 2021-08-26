---
description: A propriedade selecionada indica que os recursos já foram selecionados e que a caixa de diálogo de seleção não precisa ser mostrada. Expressões condicionais que dependem de se os recursos já estão instalados usam esse valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propriedade preselecionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a85f5c3248002fec776e45e9d7ad37550d3e16d7a5d76b098948b571b8c9c546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042316"
---
# <a name="preselected-property"></a>Propriedade preselecionada

A propriedade **selecionada** indica que os recursos já foram selecionados e que a caixa de diálogo de seleção não precisa ser mostrada.

Expressões condicionais que dependem de se os recursos já estão instalados usam esse valor. Por exemplo, a propriedade pode ser usada para suprimir qualquer caixa de diálogo que envolva seleções de recursos durante a retomada de uma instalação suspensa.

O instalador define a propriedade **preselecionada** com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades a seguir é especificada na linha de comando. Se a propriedade **preselecionada** tiver sido definida como 1, o instalador não usará a [tabela de condição](condition-table.md) para avaliar a seleção de recursos. Os recursos são instalados com base nas propriedades a seguir. O instalador sempre avalia essas propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




