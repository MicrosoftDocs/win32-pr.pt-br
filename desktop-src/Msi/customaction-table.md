---
description: A tabela CustomAction fornece os meios de integrar código e dados personalizados à instalação. A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um arquivo executável existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647355"
---
# <a name="customaction-table"></a>Tabela CustomAction

A tabela CustomAction fornece os meios de integrar código e dados personalizados à instalação. A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo recentemente instalado ou um arquivo executável existente.

A tabela CustomAction tem as colunas a seguir.



| Coluna       | Tipo                               | Chave | Nullable |
|--------------|------------------------------------|-----|----------|
| Ação       | [Identificador](identifier.md)       | S   | N        |
| Tipo         | [Inteiro](integer.md)             | N   | N        |
| Fonte       | [CustomSource](customsource.md)   | N   | S        |
| Destino       | [Binário](formatted.md)         | N   | S        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação. A ação normalmente aparece em uma tabela de sequência, a menos que seja chamada por outra ação personalizada. Se o nome corresponder a qualquer ação interna, a ação personalizada nunca será chamada.

Chave de tabela primária.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

Um campo de bits de sinalizador que especifica o tipo básico de ação e opções personalizadas. Consulte [Resumo da lista de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md) para obter uma lista dos tipos básicos. Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md), [Opções de agendamento de execução de ação](custom-action-execution-scheduling-options.md)personalizada, opção de [destino oculto de ação](custom-action-hidden-target-option.md)personalizada e opções de execução de In-Script de [ação personalizada](custom-action-in-script-execution-options.md).

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original
</dt> <dd>

Um nome de propriedade ou uma chave externa em outra tabela. Para obter uma discussão sobre as possíveis fontes de ação personalizadas, consulte [fontes de ação personalizadas](custom-action-sources.md) e a [lista de Resumo de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md). Por exemplo, a coluna de origem pode conter uma chave externa na primeira coluna de uma das tabelas a seguir contendo a origem do código de ação personalizado.

[Tabela de diretórios](directory-table.md) para chamar executáveis existentes.

[Tabela de arquivos](file-table.md) para chamar executáveis e DLLs que acabou de ser instaladas.

[Tabela binária](binary-table.md) para chamar executáveis, DLLs e dados armazenados no banco de dado.

[Tabela de propriedades](property-table.md) para chamar executáveis cujos caminhos são mantidos por uma propriedade.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

Um parâmetro de execução que depende do tipo básico de ação personalizada. Consulte a [lista de Resumo de todos os tipos de ação personalizada](summary-list-of-all-custom-action-types.md) para obter uma descrição do que deve ser inserido nesse campo para cada tipo de ação personalizada. Por exemplo, esse campo pode conter o seguinte, dependendo da ação personalizada.



| Destino                                    | Ação personalizada                         |
|-------------------------------------------|---------------------------------------|
| Ponto de entrada (obrigatório)                    | Chamando uma DLL.                        |
| Nome do executável com argumentos (obrigatório) | Chamando um executável existente.       |
| Argumentos de linha de comando (opcional)         | Chamando um executável que acabou de ser instalado. |
| Nome do arquivo de destino (obrigatório)               | Criando um arquivo a partir de dados personalizados.     |
| Nulo                                      | Executando código de script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Insira o valor de **msidbCustomActionTypePatchUninstall** nesse campo para especificar uma ação personalizada com a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md).

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. Essa opção está disponível a partir do Windows Installer 4,5.

</dd> </dl>

Para obter mais informações, consulte todos os tópicos em [ações personalizadas](custom-actions.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



