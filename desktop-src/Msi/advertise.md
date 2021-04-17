---
description: O valor da propriedade ADVERTISE é uma lista de recursos delimitados por vírgulas que devem ser anunciadas.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Propriedade ADVERTISE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783279"
---
# <a name="advertise-property"></a>Propriedade ADVERTISE

O valor da propriedade **advertise** é uma lista de recursos delimitados por vírgulas que devem ser anunciadas. Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md) . Para instalar todos os recursos como anunciados, use ADVERTISE = ALL na linha de comando. Não insira ADVERTISE = todos na tabela de [Propriedades](property-table.md) porque isso gera um pacote anunciado que não pode ser instalado ou removido.

## <a name="remarks"></a>Comentários

Observe que os nomes de recursos diferenciam maiúsculas de minúsculas.

O instalador sempre avalia as propriedades a seguir na seguinte ordem.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  **ANUNCI**
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source. Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




