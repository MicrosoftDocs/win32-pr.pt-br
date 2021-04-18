---
description: O valor da propriedade ADDLOCAL é uma lista de recursos delimitados por vírgulas e que devem ser instalados localmente.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: Propriedade ADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756745"
---
# <a name="addlocal-property"></a>Propriedade ADDLOCAL

O valor da propriedade **ADDLOCAL** é uma lista de recursos delimitados por vírgulas e que devem ser instalados localmente. Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md). Para instalar todos os recursos localmente, use ADDLOCAL = todos na linha de comando. Não insira ADDLOCAL = todos na tabela de [Propriedades](property-table.md), pois isso gera um pacote instalado localmente que não pode ser removido corretamente.

## <a name="remarks"></a>Comentários

Os nomes de recursos diferenciam maiúsculas de minúsculas. Se o sinalizador de bit SourceOnly for definido na coluna atributos da [tabela de componentes](component-table.md) para um componente de um recurso na lista, esse componente será instalado como executado da origem.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  **ADDLOCAL**
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

Por exemplo:

-   Se a linha de comando especificar: ADDLOCAL = todos, addsource = **MyFeature**, todos os recursos serão definidos primeiro como Run-local e **MyFeature** será definido como Run-from-Source.
-   Se a linha de comando for: addsource = todos, ADDLOCAL =**MyFeature**, primeiro **MyFeature** estiver definido como Run-local e, quando addsource = All for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades anteriores é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




