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

O valor da **propriedade ADDDEFAULT** é uma lista de recursos delimitados por vírgulas, que devem ser instalados em sua configuração padrão. Os recursos devem estar presentes na coluna Recurso da Tabela [de Recursos.](feature-table.md) Para instalar todos os recursos em suas configurações padrão, use ADDDEFAULT=ALL na linha de comando.

Um recurso listado na propriedade **ADDDEFAULT** é instalado no mesmo estado de instalação como se o usuário solicitava uma instalação sob demanda do recurso. O estado é determinado pelos bits definidos para o recurso na coluna Atributos da Tabela de Recursos [e](feature-table.md)quais bits são definidos para os componentes do recurso na coluna Atributos da Tabela [de Componentes](component-table.md).

## <a name="remarks"></a>Comentários

Os nomes de recursos são sensíveis a minúsculas.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Remover**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo:

-   Se a linha de comando especificar: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todos os recursos serão definidos primeiro como run-local e, em seguida, **MyFeature** será definido como run-from-source.
-   Se a linha de comando for: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primeiro **MyFeature** será definido como run-local e, em seguida, quando ADDSOURCE=ALL for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para run-from-source.

O instalador define a propriedade [**Pré-selecionada**](preselected.md) como um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




