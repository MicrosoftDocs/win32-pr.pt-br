---
description: A caixa de diálogo é redefinida. Em outras palavras, todos os controles na caixa de diálogo são chamados para desfazer as alterações de propriedade que eles executaram. Esse evento redefine todos os valores de propriedade para o que eles eram quando a caixa de diálogo foi criada.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Redefinir ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755074"
---
# <a name="reset-controlevent"></a>Redefinir ControlEvent,

A caixa de diálogo é redefinida. Em outras palavras, todos os controles na caixa de diálogo são chamados para desfazer as alterações de propriedade que eles executaram. Esse evento redefine todos os valores de propriedade para o que eles eram quando a caixa de diálogo foi criada.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Há um caso, o que deve ocorrer raramente na prática, que não é tratado corretamente por esse ControlEvent,. Se houver dois ou mais controles na mesma caixa de diálogo vinculado indiretamente à mesma propriedade e pelo menos um deles começar a ter alguma outra propriedade, esse valor de propriedade, às vezes, será redefinido para seu segundo valor.

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal é usado para redefinir todos os valores na caixa de diálogo e para cancelar todas as alterações na página.

 

 



