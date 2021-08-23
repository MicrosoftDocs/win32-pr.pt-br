---
description: A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar a sequência de aplicação de um pequeno patch de atualização em relação a todos os outros patches.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabela MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc529c0f7d1a4cdd1bab568f64507922d6e28f539636600f88dea603c4fe1a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519796"
---
# <a name="msipatchsequence-table"></a>Tabela MsiPatchSequence

A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar [a](small-updates.md) sequência de aplicação de um pequeno patch de atualização em relação a todos os outros patches. A tabela deve estar no banco de dados do arquivo de patch e não em uma transformação no patch. O instalador ignora essa tabela ao aplicar um patch [de atualização](major-upgrades.md) principal. Ao aplicar um patch [de atualização](minor-upgrades.md) secundário, o instalador usa essa tabela apenas para identificar patches substituídos que não devem ser sequenciados.

A **tabela MsiPatchSequence** tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificador](identifier.md) | Y   | N        |
| ProductCode | [GUID](guid.md)             | Y   | Y        |
| Sequência    | [Versão](version.md)       | N   | N        |
| Atributos  | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Especifica que o patch é um membro da família de patch chamada neste campo. Os patches na mesma família de patch destinados à mesma versão do produto são classificação pelos valores na coluna Sequência. Os patches dentro da família de patch são aplicados ao produto de destino na ordem de aumento da sequência. O PatchFamily também é usado para determinar quais patches devem ser superados. Um patch pode ser listado em várias linhas e pertencer a várias famílias de patch se ele se aplicar a mais de um produto ou incluir várias correções.

O Windows instalador não interpreta o valor PatchFamily de nenhuma maneira diferente das comparações de igualdade em relação a outros valores patchFamily. Um valor PatchFamily deve ser exclusivo dentro do ProductCode direcionado pelo conjunto de patches. Nos cenários de a patch complexos, o identificador PatchFamily pode precisar ser globalmente exclusivo.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>Productcode
</dt> <dd>

Um valor nesse campo é opcional. Se [um](product-codes.md) GUID de código do produto for inserido nesse campo e o patch estiver sendo aplicado ao produto especificado, o patch será classificação e aplicado como um membro do PatchFamily especificado. Se um GUID de código do produto for inserido nesse campo e o patch não estiver sendo aplicado ao produto especificado pelo ProductCode, essa linha será ignorada. Se o valor em ProductCode for NULL, o patch será classificação e aplicado como um membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.

Um patch pode ter várias linhas no mesmo PatchFamily e um ProductCode diferente para cada produto direcionado pelo patch. Uma linha para PatchFamily pode especificar NULL para ProductCode. Se o produto de destino corresponder a uma linha com um ProductCode não NULL, o instalador usará a linha correspondente e ignorará a linha com o ProductCode NULL. Se nenhum dos códigos de produto especificados corresponder ao destino, o patch será classificação e aplicado como um membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Seqüência
</dt> <dd>

O valor na coluna Sequência especifica a sequência desse patch dentro do PatchFamily especificado. O valor em Sequência é expresso no formato de [Dados de](version.md) versão. O valor contém entre 1 e 4 campos e cada campo tem um intervalo de 0 a 65535. Os membros de PatchFamily são classificação e aplicados ao produto de destino na ordem do aumento dos valores de Sequência. Por exemplo, os seis valores a seguir estão aumentando: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

A presença do atributo **msidbPatchSequenceSupersedeEarlier** em uma linha indica que o pequeno [patch](small-updates.md) de atualização substituirá as atualizações fornecidas por todos os patches com valores de sequência menores no mesmo PatchFamily. Esse patch contém todas as correções fornecidas por patches anteriores no PatchFamily especificado. Esse atributo não significa que esse patch supere os patches anteriores em todos os casos porque os patches anteriores podem pertencer a várias famílias de patch.

Um [patch de](small-updates.md) atualização pequeno [](minor-upgrades.md) não pode substituir uma atualização secundária ou um patch de [atualização](major-upgrades.md) principal em qualquer circunstâncias, mesmo que **o msidbPatchSequenceSupersedeEarlier** seja definido. 

| Nome                                   | Valor | Significado                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indica um valor de sequenciamento simples.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indica um patch que sobressede patches anteriores nesta família. |



 

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



