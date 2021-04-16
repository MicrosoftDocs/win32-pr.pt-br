---
description: O valor da propriedade COMPADDSOURCE é uma lista de GUIDs de componente da coluna ComponentID da tabela de componentes, delimitada por vírgulas, que devem ser instaladas para serem executadas a partir da mídia de origem.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Propriedade COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752263"
---
# <a name="compaddsource-property"></a>Propriedade COMPADDSOURCE

O valor da propriedade **COMPADDSOURCE** é uma lista de GUIDs de componente da coluna ComponentID da tabela de [componentes](component-table.md) , delimitada por vírgulas, que devem ser instaladas para serem executadas a partir da mídia de origem. O instalador usa esse valor para determinar quais recursos estão definidos para serem executados a partir da origem, com base nos componentes especificados. Para cada ID de componente listado, o instalador examina todos os recursos vinculados (por meio da tabela [FeatureComponents](featurecomponents-table.md) ) para esse componente e instala o recurso que requer a quantidade mínima de espaço em disco a ser instalada. Os componentes listados devem estar presentes na coluna componente da tabela de [componentes](component-table.md) .

## <a name="remarks"></a>Comentários

Observe que os nomes de componentes diferenciam maiúsculas de minúsculas. Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado localmente.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
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

 

 




