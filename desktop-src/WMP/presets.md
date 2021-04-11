---
title: Predefinições
description: Predefinições
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- visualizações, predefinições
- visualizações personalizadas, predefinições
- visualizações, predefinição de barra
- visualizações personalizadas, predefinição de barra
- visualizações, predefinição de som wave
- visualizações personalizadas, predefinição de onda
- visualizações, função render
- visualizações personalizadas, função render
- Processar função, predefinições
- visualizações, função GetPresetTitle
- visualizações personalizadas, função GetPresetTitle
- Função GetPresetTitle
- enumerações, predefinições de visualização
- visualizações, enumerações
- visualizações personalizadas, enumerações
- visualizações, cabeçalho de recurso e cadeias de caracteres
- visualizações personalizadas, cabeçalho de recurso e cadeias de caracteres
- predefinições em visualizações, predefinição de barra
- predefinições em visualizações, predefinição de onda
- predefinições em visualizações, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159665"
---
# <a name="presets"></a>Predefinições

As predefinições são fornecidas como uma maneira de ter diferentes efeitos provenientes da mesma visualização. Por exemplo, você pode criar um efeito de brilho que foi gerado por um bloco de código, mas usar uma predefinição para determinar a cor do brilho. Seus nomes predefinidos podem ser vermelho, verde e azul.

O assistente define duas predefinições para o código que ele gera. Uma é chamada de barras e a outra é chamada de onda. A predefinição de barras exibe barras que mostram a atividade no espectro de áudio e usam os dados de formato de onda. A predefinição de onda exibe uma linha de ondulação que mostra a potência de áudio da onda.

Se você alterar qualquer uma das informações predefinidas, também deverá alterar as seguintes partes do código gerado.

## <a name="render-function"></a>Função render

A função **IWMPEffects:: render** está no arquivo *ProjectName*. cpp, em que *ProjectName* é o nome do projeto que você escolheu quando executou o assistente.

O código gerado na função **render** usa uma instrução switch para escolher entre duas predefinições. A predefinição atual é qualquer que o usuário selecionar no Windows Media Player. Se você quiser alterar o código que é executado para uma predefinição específica ou adicionar ou subtrair uma predefinição, modifique a instrução switch de acordo.

As duas predefinições são definidas pelas **\_ barras predefinidas** e enumerações de **\_ escopo predefinidas** . A escolha de qual predefinição será chamada é definida por m \_ nPreset.

## <a name="getpresettitle"></a>GetPresetTitle

A função **IWMPEffects:: GetPresetTitle** está no arquivo *ProjectName*. cpp, em que *ProjectName* é o nome do projeto que você escolheu quando executou o assistente.

A função **GetPresetTitle** configura as relações entre as enumerações predefinidas e os recursos de cadeia de caracteres. As **\_ barras predefinidas** de enumerações e o **\_ escopo predefinido** são gerados pelo assistente e estão usando as IDs de recursos de cadeia de caracteres \_ BARSPRESETNAME e IDs \_ SCOPEPRESETNAME.

Você precisa alterar as enumerações e os recursos de cadeia de caracteres se adicionar, subtrair ou alterar predefinições.

## <a name="preset-enumerations"></a>Enumerações predefinidas

A enumeração predefinida é definida no arquivo *ProjectName*. h, em que *ProjectName* é o nome do projeto que você escolheu quando executou o assistente.

A enumeração define as duas predefinições atuais e a contagem. Se você adicionar ou subtrair predefinições ou alterar a enumeração, certifique-se de alterar essa enumeração para que a contagem e a ordem das predefinições estejam corretas. Essa enumeração é usada para garantir que você chame a predefinição correta na função **render** .

## <a name="resource-header"></a>Cabeçalho do recurso

Você deve definir os recursos para os nomes de sua predefinição no arquivo de cabeçalho Resource. h. As predefinições atuais são definidas como:


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Se você adicionar ou subtrair predefinições, deverá alterar o cabeçalho do recurso e os números para elas.

## <a name="resource-strings"></a>Cadeias de caracteres de recurso

Os nomes reais das predefinições são definidos no arquivo de recurso *ProjectName* dll. rc, em que *ProjectName* é o nome do projeto que você escolheu quando executou o assistente. Você pode editar esse arquivo manualmente ou usar o editor de recursos incluído com Microsoft Visual C++.

Os nomes gerados são o nome da visualização mais a predefinição específica. O arquivo de recurso para o código gerado irá defini-los como:


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



em que *ProjectName* é o nome do nome do projeto que você escolheu quando executou o assistente. É aqui que você vai alterar os nomes reais das predefinições e é assim que elas serão referenciadas e exibidas pelo Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código**](implementing-your-code.md)
</dt> </dl>

 

 




