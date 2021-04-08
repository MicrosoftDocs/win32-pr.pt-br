---
description: ICEM13 verifica se o módulo de mesclagem não contém a política do Publicador e os assemblies de configuração.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828032"
---
# <a name="icem13"></a>ICEM13

ICEM13 verifica se o módulo de mesclagem não contém a política do Publicador e os assemblies de configuração. Os assemblies de política e configuração do Publicador não devem ser incluídos em módulos de mesclagem destinados para redistribuição porque isso pode afetar outros aplicativos no computador de um usuário.

Esse ICEM está disponível no arquivo Mergemod. Cub fornecido no SDK do Windows Installer 2,0 e posterior. Para obter detalhes, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM13 posta uma mensagem de aviso se encontrar um componente especificado no campo componente da [tabela MsiAssembly](msiassembly-table.md) do módulo de mesclagem que seja uma política do Publicador ou um assembly de configuração.

## <a name="example"></a>Exemplo

ICEM13 lança a seguinte mensagem de aviso se encontrar uma linha na [tabela MsiAssembly](msiassembly-table.md) com um componente ' \[ 1 \] ' especificado no campo de componente que é uma política de editor ou assembly de configuração que foi incluído no módulo de mesclagem.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

É possível instalar a política do Publicador e os assemblies de configuração usando o Windows Installer, não é recomendável que esses assemblies sejam redistribuídos nos módulos de mesclagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



