---
description: A Tabela ModuleConfiguration identifica os atributos configuráveis do módulo. Esta tabela não é mesclada no banco de dados.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabela ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c499e313633d1668db81c91654800d1d5824192839329316f55040fd3bc7bad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963056"
---
# <a name="moduleconfiguration-table"></a>Tabela ModuleConfiguration

A Tabela ModuleConfiguration identifica os atributos configuráveis do módulo. Esta tabela não é mesclada no banco de dados.

A Tabela ModuleConfiguration tem as colunas a seguir.



| Coluna       | Tipo                         | Chave | Nullable |
|--------------|------------------------------|-----|----------|
| Nome         | [Identificador](identifier.md) | Y   | N        |
| Formatar       | [Inteiro](integer.md)       | N   | N        |
| Tipo         | [Text](text.md)             | N   | Y        |
| ContextData  | [Text](text.md)             | N   | Y        |
| DefaultValue | [Text](text.md)             | N   | Y        |
| Atributos   | [Inteiro](integer.md)       | N   | Y        |
| DisplayName  | [Text](text.md)             | N   | Y        |
| Descrição  | [Text](text.md)             | N   | Y        |
| HelpLocation | [Text](text.md)             | N   | Y        |
| HelpKeyword  | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Este campo define o nome do item configurável. Esse nome é referenciado no modelo de formatação na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Ao
</dt> <dd>

Esta coluna especifica o formato dos dados que estão sendo alterados.



| Formatar                                       | Valor |
|----------------------------------------------|-------|
| [Texto](text-format-types.md)                | 0     |
| [Chave](key-format-types.md)                  | 1     |
| [Inteiro](integer-format-types.md)          | 2     |
| [Formato de campo de bits](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

Esta coluna especifica o tipo para os dados que estão sendo alterados. Esse tipo é usado para fornecer um contexto para qualquer interface do usuário e não é usado no processo de mesclagem. Os valores válidos para essa coluna dependem do valor na coluna formato.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

Esta coluna especifica um contexto semântico para os dados solicitados. O tipo é usado para fornecer um contexto para qualquer interface do usuário e não é usado no processo de mesclagem. Os valores válidos para essa coluna dependem dos valores nas colunas Format e Type.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>ValorPadrão
</dt> <dd>

Esta coluna especifica um valor padrão para o item nesse registro se a ferramenta de mesclagem declinar para fornecer um valor. Esse valor deve ter o formato, o tipo e o contexto do item. Se esse for um item de formato "chave", a chave estrangeira deverá ser uma chave válida para as tabelas do módulo. NULL pode ser um valor válido para esta coluna, dependendo do item. Para itens de formato "chave", esse valor está no [formato especial CMSM](cmsm-special-format.md). Para todos os outros tipos, o valor é tratado literalmente.

Os autores de módulo devem garantir que o módulo seja válido em seu estado padrão. Isso garante que versões do Mergemod.dll anteriores à versão 2,0 ainda possam usar o módulo em seu estado padrão.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta coluna é um campo de bits que contém atributos para este item configurável. NULL é equivalente a 0. Todos os outros bits desta coluna são reservados para uso futuro e devem ser 0.



| Nome                             | Decimal | Hexadecimal | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | Esse atributo só se aplica a registros que listam uma chave estrangeira em uma tabela de módulo em seu campo DefaultValue. A ferramenta de mesclagem ignora o atributo para todos os formatos que não sejam os [tipos de formato de chave](key-format-types.md). Os itens não listados na [tabela ModuleSubstitution](modulesubstitution-table.md) são excluídos da verificação a seguir. A ferramenta de mesclagem não mescla a linha referenciada pela coluna DefaultValue no banco de dados de destino se as condições a seguir forem satisfeitas após a conclusão de todas as opções de configuração.<br/> Cada linha na Tabela ModuleConfiguration com o mesmo DefaultValue tem o conjunto msmConfigurationItemsKeyNoOrphan.<br/> Nenhuma linha usa DefaultValue porque a ferramenta de autor recusou a fornecer um valor.<br/> A ferramenta de mesclagem mescla a linha se qualquer uma das condições a seguir for atendida.<br/> A ferramenta de mesclagem localiza qualquer linha que não tenha msmConfigItemsKeyNoOrphan definido.<br/> Se a ferramenta de mesclagem encontrar qualquer linha usando DefaultValue porque a ferramenta de autor se recusou a fornecer um valor.<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | Quando esse atributo é definido, null não é uma resposta válida para este item. Esse atributo não tem nenhum efeito para tipos [de formato inteiro ou](integer-format-types.md) tipos de formato [bitfield](bitfield-format-types.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Esta coluna fornece uma breve descrição desse item que a ferramenta de autor pode usar na interface do usuário. Essa coluna pode não ser localizada. De definir essa coluna como nula para que o módulo seja solicitado que a ferramenta de autor não exponha essa propriedade na interface do usuário. A ferramenta pode desconsiderar o valor neste campo.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

Esta coluna fornece uma descrição desse item que a ferramenta de autor pode usar em elementos da interface do usuário. Essa cadeia de caracteres pode ser localizada pela transformação de idioma do módulo. Essa coluna pode ser nula.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

Essa coluna fornece o nome de um arquivo de ajuda (sem a extensão .chm) ou uma lista delimitada por ponto e vírgula de namespaces de ajuda. Essa coluna poderá ser nula se nenhuma ajuda estiver disponível. Essa coluna só poderá ser nula se a coluna HelpKeyword for nula.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>Helpkeyword
</dt> <dd>

Esta coluna fornece uma palavra-chave no arquivo de ajuda ou namespace da coluna HelpLocation. A interpretação dessa palavra-chave depende da coluna HelpLocation. Essa coluna pode ser nula.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela ModuleConfiguration é usada pelos [Módulos de Mesclagem Configuráveis.](configurable-merge-modules.md) Mergemod.dll 2.0 ou posterior é necessário para criar um módulo de mesclagem configurável.

Para garantir a compatibilidade com versões mais antigas do Mergemod.dll, a tabela ModuleConfiguration e a [tabela ModuleSubstitution](modulesubstitution-table.md) devem ser adicionadas à tabela [ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




