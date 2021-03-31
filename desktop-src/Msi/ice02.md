---
description: ICE02 valida que determinadas referências entre o componente, o arquivo e as tabelas do registro são recíprocas. Essas referências devem ser recíprocas para que o instalador determine corretamente o estado de instalação dos componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646808"
---
# <a name="ice02"></a>ICE02

ICE02 valida que determinadas referências entre o [componente](component-table.md), o [arquivo](file-table.md)e as tabelas [do registro](registry-table.md) são recíprocas. Essas referências devem ser recíprocas para que o instalador determine corretamente o estado de instalação dos componentes.

O instalador usa a coluna KeyPath da tabela de componentes para detectar a presença do componente listado na coluna componente. A coluna KeyPath contém uma chave para as tabelas de arquivo ou registro. Ambas as tabelas têm uma coluna de componente \_ que contém uma chave de volta para a tabela de componentes apontando para o componente que controla a entrada ou o arquivo do registro. Essas referências devem ser recíprocas.

## <a name="result"></a>Resultado

ICE02 posta uma mensagem de erro se encontrar uma referência que deve ser recíproca e não.

## <a name="example"></a>Exemplo

ICE02 publicaria a seguinte mensagem de erro para um arquivo. msi que contém as entradas de banco de dados mostradas.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Tabela de componentes](component-table.md) (parcial)



| Componente | KeyPath   |
|-----------|-----------|
| Vermelho       | \_Arquivo vermelho |
| Azul      | \_Arquivo vermelho |



 

[Tabela de arquivos](file-table.md) (parcial)



| Coluna de arquivo | Componente\_ |
|-------------|-------------|
| \_Arquivo vermelho   | Vermelho         |
| \_Arquivo azul  | Azul        |



 

O componente Blue faz referência \_ a arquivo vermelho, mas \_ o arquivo vermelho não é controlado pelo componente azul e, portanto, não pode ser o arquivo KeyPath. Se o instalador foi chamado para obter o estado de instalação de azul, ele verificaria incorretamente se o \_ arquivo vermelho foi instalado. A alteração do campo KeyPath para azul na tabela de componentes para \_ arquivo azul corrige o erro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



