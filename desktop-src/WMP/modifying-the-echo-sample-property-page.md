---
title: Modificando a página de propriedades de exemplo de eco
description: Modificando a página de propriedades de exemplo de eco
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363876"
---
# <a name="modifying-the-echo-sample-property-page"></a>Modificando a página de propriedades de exemplo de eco

A implementação da página de propriedades padrão fornecida pelo exemplo de plug-in DSP do assistente de plug-in do Windows Media Player contém um único controle de caixa de edição que recebe o fator de escala do usuário. Você precisa modificar a página de propriedades para receber os dois valores de propriedade usados pelo exemplo de eco.

Para obter uma visão geral das páginas de propriedades de plug-in do DSP, consulte [implementando um plug-in do DSP de áudio](implementing-an-audio-dsp-plug-in.md).

As seções a seguir o orientarão no processo de modificação da página de propriedades de exemplo:

-   [Modificando o recurso de diálogo de eco](modifying-the-echo-dialog-resource.md)
-   [Adicionando e modificando os eventos](adding-and-modifying-the-events.md)
-   [Como a amostra de eco persiste os dados](how-the-echo-sample-persists-data.md)
-   [Implementando CEchoPropPage:: OnInitDialog](implementing-cechoproppage--oninitdialog.md)
-   [Implementando CEchoPropPage:: apply](implementing-cechoproppage--apply.md)
-   [Implementando CEcho:: FinalConstruct](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




