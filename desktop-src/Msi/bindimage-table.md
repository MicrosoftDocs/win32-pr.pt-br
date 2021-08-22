---
description: A tabela BindImage contém informações sobre cada executável ou DLL que precisa ser associado às DLLs importadas por ele.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabela BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae4f36f3b258845bcba13748495dc9dfb53c86268bd61e98475d1c7c0c282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500757"
---
# <a name="bindimage-table"></a>Tabela BindImage

A tabela BindImage contém informações sobre cada executável ou DLL que precisa ser associado às DLLs importadas por ele.

A tabela BindImage tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Arquivo\_ | [Identificador](identifier.md) | Y   | N        |
| Caminho   | [Caminhos](paths.md)           | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Uma chave externa para a coluna um da [tabela de arquivos](file-table.md). Esse deve ser um arquivo executável ou um arquivo DLL.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Multi-Path
</dt> <dd>

Uma lista de caminhos, separados por ponto e vírgula, que representam os caminhos a serem pesquisados para localizar as DLLs importadas. A lista geralmente é uma lista de propriedades, com cada propriedade delimitada entre colchetes ( \[ \] ).

</dd> </dl>

## <a name="remarks"></a>Comentários

O instalador computa o endereço virtual de cada função importada de todas as DLLs, e o endereço virtual computado é salvo na tabela de endereços de importação da imagem de importação (IAT).

Essa tabela é referida quando a [ação de BindImage](bindimage-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



