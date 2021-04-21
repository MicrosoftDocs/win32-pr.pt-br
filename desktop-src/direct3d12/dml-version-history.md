---
title: Histórico de versão do DirectML
description: O DirectML é distribuído como um componente de sistema do Windows 10 e está disponível como parte do sistema operacional Windows 10 (SO) no Windows 10, versão 1903 (10,0; Build 18362) e mais recente.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: f5e0a478b2d4c6728a1cd53388ba09af8e5bbc0e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803936"
---
# <a name="directml-version-history"></a>Histórico de versão do DirectML

O DirectML é distribuído como um componente de sistema do Windows 10 e está disponível como parte do sistema operacional Windows 10 (SO) no Windows 10, versão 1903 (10,0; Build 18362) e mais recente.

A partir do DirectML versão 1.4.0, o DirectML também está disponível como um pacote redistribuível autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), que é útil para aplicativos que desejam usar uma versão fixa do DirectML, ou quando executados em versões anteriores do Windows 10.

DirectML segue as convenções de [controle de versão semânticos](https://semver.org/) . Ou seja, os números de versão seguem o formulário `major.minor.patch` . A primeira versão do DirectML tem uma versão do 1.0.0.

## <a name="version-table"></a>Tabela de versões

|Versão do DirectML|Nível de recurso com suporte (consulte o [histórico de nível de recurso DirectML](./dml-feature-level-history.md))|DML_TARGET_VERSION|Primeiro disponível em|Primeiro disponível em (redistribuível)|
|-|-|-|-|-|-|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|N/D|[DirectML-1.5.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/D|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, versão 2004 (10,0; Build 19041) (Windows 10 pode 2020 atualização). Também conhecido como "20H1".|N/D|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, versão 1903 (10,0; Build 18362) (Windows 10 pode 2019 atualização). Também conhecido como "19H1".|N/D|

<sup>1</sup> as versões intermediárias 1.2.0 e 1.3.0 do DirectML não foram disponibilizadas amplamente.

## <a name="selecting-a-directml-target-version"></a>Selecionando uma versão de destino DirectML

Para sua conveniência, determinados recursos no `DirectML.h` arquivo de cabeçalho são declarados condicionalmente com base no valor da `DML_TARGET_VERSION` macro. Ao definir a `DML_TARGET_VERSION` macro para determinados valores, você pode excluir partes do `DirectML.h` seu aplicativo.

Isso pode ser útil se você estiver usando uma cópia mais recente do `DirectML.h` , mas estiver visando uma versão inferior do binário DirectML, pois ele garante que qualquer tentativa de usar recursos além do nível de destino escolhido não será compilada. Esse mecanismo é semelhante à `NTDDI_VERSION` macro (consulte [macros para declarações condicionais](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).

Aqui estão os valores válidos para a `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Efeito|
|-|-|
|`0x3000`|Todos os recursos que exigem uma versão do DirectML mais recente do que o **1.4.0** são excluídos do `DirectML.h` .|
|`0x2000`|Todos os recursos que exigem uma versão do DirectML mais recente que o **1.1.0** são excluídos do `DirectML.h` .|
|`0x1000`|Todos os recursos que exigem uma versão do DirectML mais recente que a **1.0.0** são excluídos do `DirectML.h` .|
|*Não definido*|A versão de destino é selecionada automaticamente para você. Confira os detalhes abaixo.|

Se `DML_TARGET_VERSION` não estiver definido, ele será selecionado automaticamente pelo seguinte.

* Se a `DML_TARGET_VERSION_USE_LATEST` macro for definida, a versão de destino mais recente será selecionada.
* Caso contrário, a versão de destino será selecionada com base no valor da `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_19H1` resulta em uma versão de destino do `0x1000` .
  *  `NTDDI_WIN10_VB` resulta em uma versão de destino do `0x2000` .
  *  Se `NTDDI_VERSION` não estiver definido, a versão de destino mais recente será selecionada (como se `DML_TARGET_VERSION_USE_LATEST` fosse especificado).

### <a name="example"></a>Exemplo

Considere um aplicativo usando a versão 10.0.19041.0 (Windows 10, versão 2004) do SDK (Software Development Kit) do Windows. Na tabela acima, a versão do DirectML que corresponde a é 1.1.0 e o correspondente `DML_TARGET_VERSION` é `0x2000` .

Se você não definir `DML_TARGET_VERSION` nem as `NTDDI_VERSION` macros, a versão de destino selecionada usará como padrão `0x2000` e tudo estará `DirectML.h` disponível para uso.

Se você quiser que seu aplicativo seja capaz de executar no Windows 10, versão 1903 (10,0; Build 18362), em seguida, você poderia `#define DML_TARGET_VERSION 0x1000` , que excluirá todo o conteúdo `DirectML.h` que não tem suporte da versão 1.0.0 do DirectML. Isso garante que qualquer tentativa de usar a funcionalidade que requer uma versão maior não será compilada.

## <a name="directml-version-versus-feature-level"></a>Versão do DirectML versus nível de recurso

A versão DirectML (por exemplo, 1.0.0 ou 1.4.0) descreve uma versão específica do DirectML, incluindo seu arquivo `DirectML.h` de cabeçalho e `.lib` arquivo associado.

O nível de recurso (por exemplo, `DML_FEATURE_LEVEL_1_0` ou `DML_FEATURE_LEVEL_2_0` ) descreve a capacidade da implementação subjacente da API, que pode variar da versão do `DirectML.h` usada.

Por exemplo, um aplicativo com base em um SDK mais recente, mas em execução em uma versão mais antiga do Windows, pode (em tempo de execução) ver um nível de recurso com suporte inferior, mesmo que ele seja compilado em relação ao SDK mais recente.

## <a name="see-also"></a>Confira também

* [Histórico do nível de recurso do DirectML](./dml-feature-level-history.md)
* [Enumeração de DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Pacote redistribuível Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)