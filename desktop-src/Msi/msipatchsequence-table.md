---
description: A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar a sequência de aplicação de um patch de atualização pequeno em relação a todos os outros patches.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabela MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757115"
---
# <a name="msipatchsequence-table"></a>Tabela MsiPatchSequence

A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar a sequência de aplicação de um patch de [atualização pequeno](small-updates.md) em relação a todos os outros patches. A tabela deve estar no banco de dados do arquivo de patch e não em uma transformação no patch. O instalador ignora essa tabela ao aplicar um patch de [atualização importante](major-upgrades.md) . Ao aplicar um patch de [atualização secundário](minor-upgrades.md) , o instalador usa apenas essa tabela para identificar patches substituídos que não devem ser sequenciados.

A **tabela MsiPatchSequence** tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificador](identifier.md) | S   | N        |
| ProductCode | [GUID](guid.md)             | S   | S        |
| Sequência    | [Versão](version.md)       | N   | N        |
| Atributos  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Especifica que o patch é um membro da família de patches denominada neste campo. Os patches na mesma família de patches que visam a mesma versão do produto são classificados pelos valores na coluna sequência. Os patches na família de patches são aplicados ao produto de destino na ordem de crescente sequência. O PatchFamily também é usado para determinar quais patches devem ser substituídos. Um patch pode estar listado em várias linhas e pertencer a várias famílias de patches se ele se aplicar a mais de um produto ou incluir várias correções.

O Windows Installer não interpreta o valor de PatchFamily de nenhuma maneira diferente de comparações para igualdade em relação a outros valores de PatchFamily. Um valor de PatchFamily deve ser exclusivo dentro do ProductCode direcionado pelo conjunto de patches. Nos cenários de aplicação de patch complexos, o identificador PatchFamily pode precisar ser globalmente exclusivo.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

Um valor nesse campo é opcional. Se um GUID de [código de produto](product-codes.md) for inserido neste campo e o patch estiver sendo aplicado ao produto especificado, o patch será classificado e aplicado como um membro do PatchFamily especificado. Se um GUID de código do produto for inserido neste campo e o patch não estiver sendo aplicado ao produto especificado pelo ProductCode, essa linha será ignorada. Se o valor em ProductCode for nulo, o patch será classificado e aplicado como um membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.

Um patch pode ter várias linhas no mesmo PatchFamily e um ProductCode diferente para cada produto direcionado ao patch. Uma linha para PatchFamily pode especificar NULL para ProductCode. Se o produto de destino corresponder a uma linha com um ProductCode não nulo, o instalador usará a linha correspondente e ignorará a linha com o ProductCode nulo. Se nenhum dos códigos de produto especificados corresponder ao destino, o patch será classificado e aplicado como membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

O valor na coluna sequence especifica a sequência desse patch dentro do PatchFamily especificado. O valor em Sequence é expresso no formato de dados de [versão](version.md) . O valor contém entre 1 e 4 campos e cada campo tem um intervalo de 0 a 65535. Os membros de PatchFamily são classificados e aplicados ao produto de destino na ordem de valores de sequência crescente. Por exemplo, os seis valores a seguir estão aumentando: 1, 1,1, 1,2, 2, 1, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

A presença do atributo **msidbPatchSequenceSupersedeEarlier** em uma linha indica que o patch de [atualização pequeno](small-updates.md) substitui as atualizações fornecidas por todos os patches com valores de sequência menores no mesmo PatchFamily. Esse patch contém todas as correções fornecidas por patches anteriores no PatchFamily especificado. Esse atributo não significa que esse patch substitui os patches anteriores em todos os casos porque os patches anteriores podem pertencer a várias famílias de patches.

Um patch de [atualização pequeno](small-updates.md) não pode substituir um patch de atualização [secundária](minor-upgrades.md) ou de [atualização importante](major-upgrades.md) em nenhuma circunstância, mesmo que o **msidbPatchSequenceSupersedeEarlier** esteja definido. 

| Nome                                   | Valor | Significado                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indica um valor de sequenciamento simples.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indica um patch que substitui patches anteriores nesta família. |



 

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



