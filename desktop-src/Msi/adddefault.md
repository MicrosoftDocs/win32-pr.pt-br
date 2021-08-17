---
description: O valor da propriedade ADDDEFAULT é uma lista de recursos delimitados por vírgulas, que devem ser instalados em sua configuração padrão.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propriedade ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639700"
---
# <a name="adddefault-property"></a>Propriedade ADDDEFAULT

O valor da propriedade **ADDDEFAULT** é uma lista de recursos delimitados por vírgulas, que devem ser instalados em sua configuração padrão. Os recursos devem estar presentes na coluna recurso da tabela de [recursos.](feature-table.md) Para instalar todos os recursos em suas configurações padrão, use ADDDEFAULT = todos na linha de comando.

Um recurso listado na propriedade **ADDDEFAULT** é instalado no mesmo estado de instalação como se o usuário solicitasse uma instalação sob demanda do recurso. O estado é determinado pelos bits que são definidos para o recurso na coluna atributos da [tabela de recursos](feature-table.md)e quais bits são definidos para os componentes de recurso na coluna atributos da [tabela de componentes](component-table.md).

## <a name="remarks"></a>Comentários

Os nomes dos recursos diferenciam maiúsculas de minúsculas.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  **ADDDEFAULT**
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo:

-   Se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e **MyFeature** será definido como Run-from-Source.
-   Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro **MyFeature** estiver definido como Run-local e, quando addsource = All for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




