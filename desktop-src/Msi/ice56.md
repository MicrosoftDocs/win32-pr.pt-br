---
description: ICE56 valida que a estrutura de diretório do arquivo. msi tem um único diretório raiz, que a raiz é a propriedade TARGETDIR e que o valor da propriedade SourceDir está na coluna DefaultDir da tabela de diretórios.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753263"
---
# <a name="ice56"></a>ICE56

ICE56 valida que a estrutura de diretório do arquivo. msi tem um único diretório raiz, que a raiz é a propriedade [**TARGETDIR**](targetdir.md) e que o valor da propriedade [**SourceDir**](sourcedir.md) está na coluna DefaultDir da [tabela de diretórios](directory-table.md).

Se um arquivo. msi tiver várias raízes ou especificar uma raiz diferente de [**TARGETDIR**](targetdir.md), uma [instalação administrativa](administrative-installation.md) não criará uma imagem administrativa correta.

Observe que os diretórios vazios não são verificados por ICE56. A estrutura de diretório passa a validação com vários diretórios raiz se os diretórios extras estiverem vazios.

## <a name="result"></a>Resultado

ICE56 lançará um erro se o. msi não tiver uma única raiz, [**TARGETDIR**](targetdir.md)ou se [**SourceDir**](sourcedir.md) não estiver especificado na coluna DefaultDir da [tabela de diretórios](directory-table.md).

## <a name="example"></a>Exemplo

ICE56 relata os erros a seguir para o exemplo mostrado.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Tabela de diretórios](directory-table.md)



| Diretório | Pai do diretório \_ | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Para corrigir o primeiro erro, a raiz [**TARGETDIR**](targetdir.md) deve ter um valor DefaultDir de [**SourceDir**](sourcedir.md). SOURCEDIR também é aceito. Pode ser possível tornar **TARGETDIR** o pai da segunda raiz e usar o valor '. ' na coluna DefaultDir. Consulte a [tabela de diretórios](directory-table.md) para obter mais informações.

Para corrigir o segundo erro, a estrutura de diretório deve ter apenas uma raiz chamada [**TARGETDIR**](targetdir.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



