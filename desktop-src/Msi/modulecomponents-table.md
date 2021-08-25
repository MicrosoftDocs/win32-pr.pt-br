---
description: A tabela ModuleComponents contém uma lista dos componentes encontrados no módulo de mesclagem.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabela ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926476"
---
# <a name="modulecomponents-table"></a>Tabela ModuleComponents

A tabela ModuleComponents contém uma lista dos componentes encontrados no módulo de mesclagem.

A tabela ModuleComponents tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Componente | [Identificador](identifier.md) | Y   | N        |
| ModuleID  | [Identificador](identifier.md) | Y   | N        |
| Idioma  | [Inteiro](integer.md)       | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Um identificador que faz referência a um componente no módulo de mesclagem. A coluna de componente é uma chave estrangeira para a [tabela de componentes](component-table.md). A entrada na coluna componente deve seguir a Convenção de nomenclatura na [nomenclatura de chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

O identificador do módulo de mesclagem. Esta é uma chave estrangeira para a [tabela ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

O identificador de idioma descreve o idioma padrão para o módulo de mesclagem. O identificador de idioma está em formato decimal, por exemplo, o inglês dos EUA é 1033. Chave estrangeira para a [tabela ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As transformações de linguagem devem ser capazes de atualizar esta tabela se o módulo de mesclagem oferecer suporte a vários idiomas.

 

 



