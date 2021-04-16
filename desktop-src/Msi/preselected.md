---
description: A propriedade selecionada indica que os recursos já foram selecionados e que a caixa de diálogo de seleção não precisa ser mostrada. Expressões condicionais que dependem de se os recursos já estão instalados usam esse valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propriedade preselecionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750226"
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
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




