---
description: Essa tabela temporária habilita a Opção de Desinstalação de Patch de Ação Personalizada para ações personalizadas adicionadas ou atualizadas por um patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b6c46ebfcfb82ee23ce6acec998490f53fe67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882236"
---
# <a name="msitransformview"></a>MsiTransformView

Essa tabela temporária habilita a [Opção de Desinstalação](custom-action-patch-uninstall-option.md) de Patch de Ação Personalizada para ações personalizadas adicionadas ou atualizadas por um patch.

Se um patch adiciona ou atualiza uma ação personalizada com o atributo **msidbCustomActionTypePatchUninstall,** o Windows Installer executa a ação personalizada nova ou atualizada quando o patch é desinstalado. Windows O instalador disponibiliza as atualizações dentro do patch que está sendo desinstalado para a ação personalizada de desinstalação de patch. O patch deve incluir uma tabela *&lt; PatchGUID &gt;* MsiTransformView para fornecer essas informações ao Windows Instalador. As informações nesta tabela estão disponíveis para qualquer ação personalizada imediata e não estão disponíveis para ações personalizadas adiadas.

**[Windows Instalador 4.0 e anterior:](not-supported-in-windows-installer-4-0.md)** Sem suporte. A [Opção de Desinstalação](custom-action-patch-uninstall-option.md) de Patch de Ação Personalizada está disponível a partir do Windows Installer 4.5.

Essa tabela deve ser denominada Tabela *&lt; PatchGUID &gt;* MsiTransformView, em que *&lt; PatchGUID &gt;* é o GUID que identifica exclusivamente o patch. A Tabela *&lt; PatchGUID &gt;* MsiTransformView tem as seguintes colunas.



| Coluna  | Tipo                         | Chave | Nullable |
|---------|------------------------------|-----|----------|
| Tabela   | [Identificador](identifier.md) | S   | N        |
| Coluna  | [Text](text.md)             | S   | N        |
| Linha     | [Text](text.md)             | S   | S        |
| Dados    | [Text](text.md)             | N   | S        |
| Current | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Nome de uma tabela de banco de dados alterada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Coluna
</dt> <dd>

Nome de uma coluna de tabela alterada ou INSERT, DELETE, CREATE ou DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Linha
</dt> <dd>

Uma lista dos valores de chave primária separados por guias. Valores de chave primária nulos são representados por um único caractere de espaço. Um valor Nulo nesta coluna indica uma alteração de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dados
</dt> <dd>

Dados, nome de um fluxo de dados ou uma definição de coluna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Atual
</dt> <dd>

Valor atual do banco de dados de referência ou coluna um número.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ações personalizadas de desinstalação de patch são executados quando o patch é desinstalado. Eles não são executados quando o produto é desinstalado. Use a [Opção de Desinstalação](custom-action-patch-uninstall-option.md) de Patch de Ação Personalizada e esta tabela para executar um personalizado somente quando o patch estiver sendo desinstalado.

Um patch pode atualizar uma ação personalizada fornecida no pacote original (.msi arquivo).) Para executar a versão atualizada da ação personalizada quando o patch for desinstalado, marque a ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** no pacote original.

 

 



