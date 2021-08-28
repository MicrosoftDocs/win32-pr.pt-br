---
description: A tabela CustomAction fornece o meio de integrar código personalizado e dados à instalação. A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo instalado recentemente ou um arquivo executável existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725ac6ad72b1f84da2c43c94a91cd4a466bd02a5af19261b4b07dfd1c496ae76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947860"
---
# <a name="customaction-table"></a>Tabela CustomAction

A tabela CustomAction fornece o meio de integrar código personalizado e dados à instalação. A origem do código que é executado pode ser um fluxo contido no banco de dados, um arquivo instalado recentemente ou um arquivo executável existente.

A tabela CustomAction tem as seguintes colunas.



| Coluna       | Tipo                               | Chave | Nullable |
|--------------|------------------------------------|-----|----------|
| Ação       | [Identificador](identifier.md)       | Y   | N        |
| Tipo         | [Inteiro](integer.md)             | N   | N        |
| Fonte       | [Customsource](customsource.md)   | N   | Y        |
| Destino       | [Formatado](formatted.md)         | N   | Y        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Ação
</dt> <dd>

Nome da ação. A ação normalmente aparece em uma tabela de sequência, a menos que seja chamada por outra ação personalizada. Se o nome corresponde a qualquer ação integrada, a ação personalizada nunca é chamada.

Chave de tabela primária.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Um campo de bits de sinalizador que especifica o tipo básico de ações e opções personalizadas. Consulte [Lista resumida de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md) para ver uma lista dos tipos básicos. Consulte [Opções de processamento de retorno de](custom-action-return-processing-options.md)ação personalizada, Opções de agendamento de execução de ação personalizada, opção de destino oculto de ação personalizada e ações personalizadas In-Script opções de [execução](custom-action-in-script-execution-options.md). [](custom-action-execution-scheduling-options.md) [](custom-action-hidden-target-option.md)

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fonte
</dt> <dd>

Um nome de propriedade ou chave externa em outra tabela. Para uma discussão sobre as possíveis fontes de ação personalizadas, consulte Fontes [de ação personalizadas](custom-action-sources.md) e a lista [de resumos de todos os tipos de ação personalizados.](summary-list-of-all-custom-action-types.md) Por exemplo, a coluna Source pode conter uma chave externa na primeira coluna de uma das tabelas a seguir que contém a origem do código de ação personalizado.

[Tabela de](directory-table.md) diretório para chamar executáveis existentes.

[Tabela de](file-table.md) arquivos para chamar executáveis e DLLs que foram instaladas.

[Tabela binária](binary-table.md) para chamar executáveis, DLLs e dados armazenados no banco de dados.

[Tabela de](property-table.md) propriedades para chamar executáveis cujos caminhos são mantidos por uma propriedade .

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

Um parâmetro de execução que depende do tipo básico de ação personalizada. Consulte a [Lista resumida de todos os tipos de](summary-list-of-all-custom-action-types.md) ação personalizados para ver uma descrição do que deve ser inserido nesse campo para cada tipo de ação personalizada. Por exemplo, esse campo pode conter o seguinte, dependendo da ação personalizada.



| Destino                                    | Ação personalizada                         |
|-------------------------------------------|---------------------------------------|
| Ponto de entrada (obrigatório)                    | Chamando uma DLL.                        |
| Nome executável com argumentos (obrigatório) | Chamar um executável existente.       |
| Argumentos de linha de comando (opcional)         | Chamar um executável que acabou de ser instalado. |
| Nome do arquivo de destino (obrigatório)               | Criando um arquivo de dados personalizados.     |
| Nulo                                      | Executando o código de script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Insira o **valor msidbCustomActionTypePatchUninstall** neste campo para especificar uma ação personalizada com a Opção de Desinstalação de Patch de Ação [Personalizada](custom-action-patch-uninstall-option.md).

**[Windows Instalador 4.0 e anterior:](not-supported-in-windows-installer-4-0.md)** Sem suporte. Essa opção está disponível a partir do Windows Installer 4.5.

</dd> </dl>

Para obter mais informações, consulte todos os tópicos em [Ações Personalizadas.](custom-actions.md)

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

 

 



