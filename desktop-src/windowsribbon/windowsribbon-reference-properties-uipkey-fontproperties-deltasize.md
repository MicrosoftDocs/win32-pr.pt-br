---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica a propriedade \_ \_ FontProperties DeltaSize da PKEY da interface do \_ usuário.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35d2660d2221b4edad567b0fd05eb8283fce4b3cc7d1cb8e35c735838f385d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438744"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>Interface \_ do usuário \_ FontProperties \_ DeltaSize

Identifica a propriedade \_ \_ FontProperties DeltaSize da PKEY da interface do \_ usuário.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ \_ PKEY FontProperties \_ DeltaSize é usada por um aplicativo em casos em que não é possível que o aplicativo especifique um valor para Tamanho da fonte, como quando uma operação de texto de tamanho heterogêneo é selecionada. O **controle** Tamanho da fonte é definido como em branco e \_ \_ FontProperties \_ DeltaSize   da interface do usuário É usado para capturar a interação do usuário com os botões Aumentar fonte e Reduzir fonte.

UI PKEY FontProperties DeltaSize está incluído na interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

A captura de tela a seguir mostra os **botões Crescimento da** fonte e **Redução** de fonte do FontControl da Faixa [**de Opções.**](windowsribbon-element-fontcontrol.md)

![captura de tela dos botões de redução de fonte e de crescimento de fonte no controle de fonte.](images/markup/fontcontrol-incdec.png)

A tabela a seguir descreve os valores da propriedade.



|     Valor                 |  Descrição                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | **Botão Aumentar fonte** clicado.   |
| `UI_FONTDELTASIZE_SHRINK` | **Botão Reduzir** fonte clicado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTDELTASIZE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 