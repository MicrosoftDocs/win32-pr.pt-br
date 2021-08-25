---
description: ICEM13 verifica se o módulo de mesclagem não contém assemblies de configuração e política de editor.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678b89e14cb699bb6207be5c2e14473de2a743494b47ff5ae5e0ccda2a9cc9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894276"
---
# <a name="icem13"></a>ICEM13

ICEM13 verifica se o módulo de mesclagem não contém assemblies de configuração e política de editor. Publisher assemblies de configuração e política não devem ser incluídos em módulos de mesclagem destinados à redistribuição, pois isso pode afetar outros aplicativos no computador de um usuário.

Esse ICEM está disponível no arquivo Mergemod.file fornecido no SDK do Windows Installer 2.0 e posterior. Para obter detalhes, consulte [Windows SDK components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM13 posta uma mensagem de aviso se encontrar um componente especificado no campo Componente da Tabela [MsiAssembly](msiassembly-table.md) do módulo de mesclagem que é uma política de editor ou assembly de configuração.

## <a name="example"></a>Exemplo

ICEM13 posta a seguinte mensagem de aviso se encontrar uma linha na Tabela [MsiAssembly](msiassembly-table.md) com um componente ' 1 ' especificado no campo Componente que é uma política de editor ou assembly de configuração que foi incluído no módulo de \[ mesclagem. \]

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

É possível instalar assemblies de política e configuração do publicador usando o instalador Windows, não é recomendável que esses assemblies sejam redistribuídos em módulos de mesclagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



