---
description: Essa tabela temporária habilita a opção de desinstalação de patch de ação personalizada para ações personalizadas adicionadas ou atualizadas por um patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978f27fe68d89abd3ea94a4d13adc815bbc6510564caf949b937d8a4213428b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944244"
---
# <a name="msitransformview"></a>MsiTransformView

Essa tabela temporária habilita a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) para ações personalizadas adicionadas ou atualizadas por um patch.

se um patch adicionar ou atualizar uma ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** , Windows Installer executará a ação personalizada nova ou atualizada quando o patch for desinstalado. Windows O instalador faz com que as atualizações no patch sejam desinstaladas disponíveis para a ação personalizada de desinstalação do patch. o patch deve incluir uma *<PatchGUID>* tabela MsiTransformView para fornecer essas informações para Windows Installer. As informações nesta tabela estão disponíveis para qualquer ação personalizada imediata e não estão disponíveis para ações personalizadas adiadas.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. a [opção de desinstalação de Patch de ação personalizada](custom-action-patch-uninstall-option.md) está disponível a partir do Windows Installer 4,5.

Essa tabela deve ser nomeada como *<PatchGUID>* tabela MsiTransformView, em que *<PatchGUID>* é o GUID que identifica exclusivamente o patch. A *<PatchGUID>* tabela MsiTransformView tem as colunas a seguir.



| Coluna  | Tipo                         | Chave | Nullable |
|---------|------------------------------|-----|----------|
| Tabela   | [Identificador](identifier.md) | Y   | N        |
| Coluna  | [Text](text.md)             | Y   | N        |
| Linha     | [Text](text.md)             | Y   | Y        |
| Dados    | [Text](text.md)             | N   | Y        |
| Current | [Text](text.md)             | N   | Y        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Nome de uma tabela de banco de dados alterada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha
</dt> <dd>

Nome de uma coluna de tabela alterada ou inserir, excluir, criar ou descartar.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Uma lista dos valores de chave primária separados por tabulações. Valores nulos de chave primária são representados por um único caractere de espaço. Um valor nulo nesta coluna indica uma alteração de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Dados, nome de um fluxo de dados ou uma definição de coluna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Atualizados
</dt> <dd>

Valor atual do banco de dados de referência ou de um número de coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

O patch de desinstalação de ações personalizadas é executado quando o patch é desinstalado. Eles não são executados quando o produto é desinstalado. Use a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) e esta tabela para executar um personalizado somente quando o patch estiver sendo desinstalado.

Um patch pode atualizar uma ação personalizada fornecida no pacote original (.msi arquivo). Para executar a versão atualizada da ação personalizada quando o patch for desinstalado, marque a ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** no pacote original.

 

 



