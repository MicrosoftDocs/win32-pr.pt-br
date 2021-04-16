---
description: Esse atributo mede a distância em que a barra de indicadores de progresso é preenchida.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de controle de progresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750604"
---
# <a name="progress-control-attribute"></a>Atributo de controle de progresso

Esse atributo mede a distância em que a barra de indicadores de progresso é preenchida. O registro contém dois inteiros e uma cadeia de caracteres. O primeiro número é o andamento, o segundo número é o intervalo (o número máximo possível para o andamento). Na configuração, os inteiros podem ser inseridos como campos inteiros ou cadeias de caracteres que contêm os inteiros. Se o segundo número estiver ausente, supõe-se que seja o padrão (1024). Se o progresso for maior do que o intervalo, ele será alterado para ser o intervalo. O terceiro campo é uma cadeia de caracteres, o nome da ação cujo progresso é exibido.

Para obter informações relacionadas, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md)e [adicionando ações personalizadas ao ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Controles válidos

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Sinalizadores de bits associados

Este atributo não usa sinalizadores de bit.

## <a name="remarks"></a>Comentários

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



