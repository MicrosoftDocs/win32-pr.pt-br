---
description: O valor da propriedade COMPADDLOCAL é uma lista de GUIDs de componente da coluna ComponentID da tabela de componentes, delimitada por vírgulas, que devem ser instaladas localmente.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: Propriedade COMPADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e403459f0355c28d66da00170b9c649084afbb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756738"
---
# <a name="compaddlocal-property"></a>Propriedade COMPADDLOCAL

O valor da propriedade **COMPADDLOCAL** é uma lista de GUIDs de componente da coluna ComponentID da tabela de [componentes](component-table.md), delimitada por vírgulas, que devem ser instaladas localmente. O instalador usa essa lista para determinar quais recursos estão definidos para serem instalados localmente, com base nos componentes especificados. Para cada ID de componente listado, o instalador examina todos os recursos vinculados a esse componente por meio da tabela [FeatureComponents](featurecomponents-table.md) e instala o recurso que requer a quantidade mínima de espaço em disco a ser instalada. Os componentes listados devem estar presentes na coluna componente da tabela de [componentes](component-table.md) .

## <a name="remarks"></a>Comentários

Observe que os nomes de componentes diferenciam maiúsculas de minúsculas. Observe também que, se o sinalizador de bit SourceOnly for definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado da origem.

O instalador sempre avalia as propriedades a seguir na seguinte ordem.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  **COMPADDLOCAL**
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

 

 




