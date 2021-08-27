---
description: ICE76 verifica o uso do catálogo SFP (WFP) em pacotes Windows Installer para Windows mim. Essa ICE também verifica se nenhum arquivo na tabela BindImage referencia catálogos SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0b6caf5e29d26ba68721daa156dd0fc78a1868b5aa1ba1b7ea165834dd5ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129426"
---
# <a name="ice76"></a>ICE76

ICE76 verifica o uso do catálogo SFP (WFP) em pacotes Windows Installer para Windows mim. Essa ICE também verifica se nenhum arquivo na [tabela](bindimage-table.md) BindImage referencia catálogos SFP.

Windows A proteção de arquivo requer uma correspondência exata entre o arquivo e a assinatura inserida no arquivo de catálogo. Os arquivos que fazem referência a um catálogo do SFP não devem ser listados na tabela BindImage porque o efeito da [ação de BindImage](bindimage-action.md) nesses arquivos é diferente entre os computadores. Os arquivos referenciados por catálogos do SFP devem estar em componentes que são permanentes ou instalados localmente.

## <a name="result"></a>Resultado

ICE76 posta um erro para cada arquivo na [tabela BindImage](bindimage-table.md) que também está na [tabela FileSFPCatalog](filesfpcatalog-table.md).

ICE76 gera um erro se um arquivo na tabela FileSFPCatalog pertencer a um componente com qualquer um dos seguintes verdadeiros:

-   **msidbComponentAttributesPermanent** não está definido na coluna Attributes da [tabela Component](component-table.md).
-   **msidbComponentAttributesSourceOnly** é definido na coluna Attributes da tabela Component.
-   **msidbAttributesOptional** é definido na coluna Attributes da tabela Component.

## <a name="example"></a>Exemplo

ICE76 relata o seguinte erro para o exemplo:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Tabela FileSFPCatalog](filesfpcatalog-table.md) (parcial)



| Arquivo\_ | SFPCatalog\_ |
|--------|--------------|
| Arquivo1  | Catalog1.Cat |



 

[Tabela BindImage](bindimage-table.md) (parcial)



| Arquivo\_ |
|--------|
| Arquivo1  |



 

Para corrigir isso, não insira nenhum arquivo que referencie catálogos SFP na tabela BindImage.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela BindImage](bindimage-table.md)
</dt> <dt>

[Tabela de componentes](component-table.md)
</dt> <dt>

[Tabela FileSFPCatalog](filesfpcatalog-table.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



