---
title: Unidades VML
description: Este artigo descreve as unidades da VML. a VML é um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c510bacd2081fb5a051637b6b577fc9415662737d384d10d7c3dd73348c694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597377"
---
# <a name="vml-units"></a>Unidades VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

As seguintes unidades CSS são usadas pelo VML.



Unidades de comprimento relativo

duplo

A altura da fonte do elemento.

Estendi

A altura da letra "x".

px

Pixels.

%

Porcentagem.

Unidades de comprimento absoluto

in

Polegadas (1 polegada = 2,54 centímetros).

cm

Centímetros.

MM

Milímetros.

pt

Pontos (1 ponto = 1/72 polegadas).

pc

Paicas (1 paica = 12 pontos).



 

As medidas e as posições nas propriedades da folha de estilos em cascata (CSS) são feitas usando unidades de comprimento. O Internet Explorer dá suporte a dois tipos de unidades de comprimento: relativo e absoluto.

Uma unidade de comprimento relativo especifica um comprimento em relação a outra propriedade de comprimento. A escala de unidades de comprimento relativo é melhor de um dispositivo de saída para outro, como de um monitor para uma impressora. As porcentagens e as palavras-chave são executadas da mesma forma.

Uma unidade de comprimento absoluto especifica uma medida absoluta, como polegadas ou centímetros. Unidades de comprimento absoluto são úteis quando as propriedades físicas do dispositivo de saída são conhecidas.

## <a name="other-units-of-measurement"></a>Outras unidades de medida

**MONETÁRIA**

A EMU (unidade de métrica em inglês) é a menor unidade de medida útil e é usada pelo VML para armazenamento de unidade interna. Há 914400 EMU por polegada e 12700 da EMU em um ponto. EMUs não pode ser fracionário.

Como EMUs são definidos por números integrais assinados de 32 bits, o maior número de EMUs é de 2348 polegadas (cerca de 59 metros ou 65 metros). Como as medidas sempre serão ajustadas em um dispositivo de saída de tela ou de página, elas sempre estarão dentro desse intervalo.

**Ângulos**

As medidas de ângulo podem ser definidas com os seguintes sufixos.



Sufixo

FD

Graus fracionários.

nenhum

Degrees

deg

Degrees

rad

Radians



 

 

 