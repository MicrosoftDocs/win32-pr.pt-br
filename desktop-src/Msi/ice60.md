---
description: O ICE60 valida a tabela Arquivo de um banco de Windows do Instalador.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8d2cbf9136ea6195a138c586d4408dc0d2e5ff411b52fd73fec8a569c5d186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044026"
---
# <a name="ice60"></a>ICE60

O ICE60 verifica se os arquivos na tabela [Arquivo atendem](file-table.md) à seguinte condição:

-   Se o arquivo não for uma fonte e tiver uma versão, ele deverá ter um idioma.
-   ICE60 verifica se nenhum arquivo com controle de versão está listado na [tabela MsiFileHash](msifilehash-table.md).

A falha ao corrigir um aviso relatado pelo ICE60 geralmente leva a um arquivo ser reinstalado descaradamente quando um reparo do produto é feito. Isso acontece porque o arquivo a ser instalado no reparo e o arquivo existente no disco têm a mesma versão (eles são o mesmo arquivo), mas idiomas diferentes. A tabela de arquivos lista o idioma como nulo, mas o próprio arquivo tem um valor de idioma no recurso. Com base nas [regras de versão do arquivo](file-versioning-rules.md), o instalador favorece que o arquivo seja instalado, portanto, ele é recopiado de forma desnecessário.

## <a name="result"></a>Resultado

ICE60 posta um aviso ou um [](file-table.md) erro se um arquivo na tabela Arquivo que não é uma fonte e tem uma versão, não tem um idioma.

ICE60 postará o seguinte erro se um arquivo listado na tabela MsiFileHash tiver versão.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Exemplo

O ICE60 relata o seguinte erro e aviso para o exemplo mostrado. (O arquivo B é uma fonte; os outros arquivos não são.)

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

FileA tem uma versão e um idioma; portanto, nenhum aviso ou erro é gerado.

O FileB tem uma versão, mas nenhum idioma. Nenhum aviso ou erro é gerado, no entanto, porque é uma fonte.

O FileC é uma referência a mais, portanto, ele não precisa ter um idioma. Nenhum aviso ou erro é gerado.

O FileD não tem nenhuma versão, portanto, ele não precisa ter um idioma. Nenhum aviso ou erro é gerado.

O FileE tem uma versão, mas nenhum idioma. Portanto, um aviso é gerado.

Para corrigir esse aviso, adicione um idioma ao FileE.

Os arquivos devem ter valores de idioma armazenados no recurso de versão sempre que possível. Se um arquivo for neutro no idioma, use [o LANGID](column-data-types.md) 0.

[Tabela de](file-table.md) Arquivos (FileB é uma fonte; os outros arquivos não são.)



| Arquivo  | Versão | Idioma |
|-------|---------|----------|
| FileA | 1.0     | 1046     |
| FileB | 1.0     |          |
| FileC | FileA   |          |
| Arquivado |         |          |
| FileE | 1.0     |          |



 

[Tabela de fontes](font-table.md)



| Arquivo  | FontTitle  |
|-------|------------|
| FileB | Título da fonte |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



