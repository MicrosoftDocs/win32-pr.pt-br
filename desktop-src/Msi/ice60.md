---
description: ICE60 valida a tabela de arquivos de um banco de dados Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756728"
---
# <a name="ice60"></a>ICE60

ICE60 verifica se os arquivos na [tabela de arquivos](file-table.md) atendem à seguinte condição:

-   Se o arquivo não for uma fonte e tiver uma versão, ele deverá ter um idioma.
-   ICE60 verifica se nenhum arquivo com versão está listado na [tabela MsiFileHash](msifilehash-table.md).

A falha em corrigir um aviso relatado por ICE60 geralmente leva a um arquivo desinstalado desnecessariamente quando um reparo do produto é feito. Isso acontece porque o arquivo a ser instalado no reparo e o arquivo existente no disco têm a mesma versão (eles são o mesmo arquivo), mas idiomas diferentes. A tabela de arquivos lista o idioma como nulo, mas o próprio arquivo tem um valor de idioma no recurso. Com base nas [regras de controle de versão de arquivo](file-versioning-rules.md), o instalador favorece o arquivo a ser instalado e, portanto, é recopiado desnecessariamente.

## <a name="result"></a>Resultado

ICE60 lançará um aviso ou um erro se um arquivo na [tabela de arquivos](file-table.md) que não é uma fonte e tiver uma versão não tiver uma linguagem.

ICE60 lançará o erro a seguir se um arquivo listado na tabela MsiFileHash tiver controle de versão.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Exemplo

ICE60 relata o seguinte erro e aviso para o exemplo mostrado. (O arquivo B é uma fonte; os outros arquivos não são.)

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

O arquivoA tem uma versão e um idioma; Portanto, nenhum aviso ou erro é gerado.

FileB tem uma versão, mas não idioma. No entanto, nenhum aviso ou erro é gerado porque é uma fonte.

FileC é uma referência complementar, portanto, não precisa ter um idioma. Nenhum aviso ou erro é gerado.

O Arquivado não tem nenhuma versão, portanto, não precisa ter um idioma. Nenhum aviso ou erro é gerado.

O arquivo tem uma versão, mas não idioma. Portanto, um aviso é gerado.

Para corrigir esse aviso, adicione um idioma para o arquivo.

Os arquivos devem ter valores de idioma armazenados no recurso de versão sempre que possível. Se um arquivo for de idioma neutro, use o [LangID](column-data-types.md) 0.

A [tabela de arquivos](file-table.md) (FileB é uma fonte; os outros arquivos não são.)



| Arquivo  | Versão | Idioma |
|-------|---------|----------|
| FileA | 1.0     | 1046     |
| FileB | 1.0     |          |
| FileC | FileA   |          |
| Arquiva |         |          |
| Arquivo | 1.0     |          |



 

[Tabela de fontes](font-table.md)



| Arquivo  | FontTitle  |
|-------|------------|
| FileB | Título da fonte |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



