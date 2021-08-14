---
description: O valor da propriedade ADVERTISE é uma lista de recursos delimitados por vírgulas que devem ser anunciados.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Propriedade ADVERTISE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da43d291b64ed10c1ae5321a766eca6cab9c4423a26625aacd92e9591d2e3f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381595"
---
# <a name="advertise-property"></a>Propriedade ADVERTISE

O valor da **propriedade ADVERTISE** é uma lista de recursos delimitados por vírgulas que devem ser anunciados. Os recursos devem estar presentes na coluna Recurso da [tabela](feature-table.md) Recurso. Para instalar todos os recursos conforme anunciado, use ADVERTISE=ALL na linha de comando. Não insira ADVERTISE=ALL na tabela [Propriedade](property-table.md) porque isso gera um pacote anunciado que não pode ser instalado ou removido.

## <a name="remarks"></a>Comentários

Observe que os nomes de recursos são sensíveis a minúsculas.

O instalador sempre avalia as propriedades a seguir na ordem a seguir.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Remover**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  **Anunciar**
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
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

 

 




