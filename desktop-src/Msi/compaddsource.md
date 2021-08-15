---
description: O valor da propriedade COMPADDSOURCE é uma lista de GUIDs de componente da coluna ComponentId da tabela Component, delimitada por vírgulas, que devem ser instaladas para serem executados da mídia de origem.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Propriedade COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f68e795a9092892212f41a073a8e5a80945f57be14224e576262c30bba92707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380048"
---
# <a name="compaddsource-property"></a>Propriedade COMPADDSOURCE

O valor da propriedade **COMPADDSOURCE** é uma lista de GUIDs de componente da coluna ComponentId da tabela [Component,](component-table.md) delimitada por vírgulas, que devem ser instaladas para serem executados da mídia de origem. O instalador usa esse valor para determinar quais recursos estão definidos para serem instalados para serem executados da origem, com base nos componentes especificados. Para cada ID de componente listada, o instalador examina todos os recursos vinculados (por meio da tabela [FeatureComponents)](featurecomponents-table.md) a esse componente e instala o recurso que requer a menor quantidade de espaço em disco a ser instalada. Os componentes listados devem estar presentes na coluna Componente da [tabela](component-table.md) Componente.

## <a name="remarks"></a>Comentários

Observe que os nomes de componente diferenciam minúsculas. Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna Atributos da tabela Componente de um componente, o componente será instalado para ser executado localmente. [](component-table.md)

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Remover**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo, se a linha de comando especificar: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todos os recursos serão definidos primeiro como run-local e, em seguida, MyFeature será definido como run-from-source. Se a linha de comando for: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primeiro MyFeature será definido como run-local e, em seguida, quando ADDSOURCE=ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para run-from-source.

O instalador define a propriedade [**Pré-selecionada**](preselected.md) como um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




