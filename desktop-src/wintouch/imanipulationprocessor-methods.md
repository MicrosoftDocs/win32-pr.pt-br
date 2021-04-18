---
title: Métodos (IInertiaProcessor)
description: Esta seção contém os métodos para a interface IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interface IInertiaProcessor
- Windows Touch, métodos de interface
- inércia, interface IInertiaProcessor
- Interface IInertiaProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771378"
---
# <a name="methods-iinertiaprocessor"></a>Métodos (IInertiaProcessor)

Esta seção contém os métodos para a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Método                                                 | Descrição                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Redefinir**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Inicializa o processador com o carimbo de data/hora inicial e reinicia o inércia.                                                                                                                                                    |
| [**Processar**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Executa cálculos para o tique atual e pode gerar o **Delta** ou o evento **concluído** dependendo se a extrapolação está concluída ou não. Se a extrapolação terminar no tique anterior, o método será no-op. |
| [**Processtime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Executa cálculos para a marcação especificada e pode gerar o evento **Delta** ou **Completed** dependendo se a extrapolação está concluída ou não.                                                                        |
| [**Concluir**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Conclui a manipulação atual e para o inércia no processador inércia.                                                                                                                                              |
| [**Concluído**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Conclui a manipulação atual no tique especificado, interrompe o inércia no processador inércia e gera o evento ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




