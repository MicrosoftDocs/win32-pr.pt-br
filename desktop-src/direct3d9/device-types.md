---
description: Tipos de dispositivo (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Tipos de dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295974"
---
# <a name="device-types-direct3d-9"></a>Tipos de dispositivo (Direct3D 9)

## <a name="hal-device"></a>Dispositivo HAL

O tipo de dispositivo principal é o dispositivo hal, que dá suporte à rasterização acelerada por hardware e ao processamento de vértice de hardware e software. Se o computador no qual seu aplicativo está sendo executado é equipado com um adaptador de vídeo compatível com o Direct3D, seu aplicativo deve usá-lo para as operações do Direct3D. Os dispositivos hal com Direct3D implementam todos ou parte dos módulos de rasterização, iluminação e transformação no hardware.

Os aplicativos não acessam os adaptadores gráficos diretamente. Eles chamam métodos e funções do Direct3D. O Direct3D acessa o hardware por meio do hal. Se o computador que seu aplicativo está sendo executado oferece suporte a hal, ele obterá o melhor desempenho usando um dispositivo hal.

Para criar um dispositivo Hal, chame [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) usando \_ o Hal D3DDEVTYPE como o tipo de dispositivo.

## <a name="reference-device"></a>Dispositivo de referência

O Direct3D dá suporte a um tipo de dispositivo adicional chamado um rasterizador de referência ou dispositivo de referência. Ao contrário de um dispositivo de software, o rasterizador de referência dá suporte a todos os recursos do Direct3D. Este dispositivo se destina a ser usado para fins de depuração e, portanto, só está disponível em computadores em que o SDK do DirectX tiver sido instalado. Como esses recursos são implementados para precisão em vez de velocidade e são implementados no software, os resultados não são muito rápidos. O rasterizador de referência faz uso de instruções especiais da CPU sempre que possível, mas ele não foi desenvolvido para aplicativos de varejo. Use o rasterizador de referência apenas para fins de teste ou demonstração do recurso. Para criar um dispositivo de referência, chame o método [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) usando D3DDEVTYPE \_ ref como o tipo de dispositivo.

## <a name="hal-vs-ref-devices"></a>Dispositivos HAL vs. REF

Os dispositivos HAL (camada de abstração de Hardware) e REF (rasterizador de referência) são os dois tipos principais de dispositivo Direct3D; o primeiro baseia-se no suporte de hardware e é muito rápido, mas talvez não dê suporte a tudo; enquanto o segundo usa a aceleração de hardware, portanto é muito lento, mas garante suporte a todo o conjunto de recursos do Direct3D, da forma correta. Em geral, você só precisará usar dispositivos HAL, mas se você estiver usando algum recurso avançado que não dá suporte à placa gráfica, então talvez seja necessário voltar ao REF.

Uma outra ocasião onde convém usar o REF é se o dispositivo HAL estiver produzindo resultados estranhos, ou seja, você tem certeza que seu código está correto, mas o resultado não é o que você espera. É garantido que o dispositivo REF irá se comportar corretamente, portanto, convém testar seu aplicativo no dispositivo REF e ver se o comportamento estranho continua. Se isso não acontecer, isso significa que o seu aplicativo está pressupondo que a placa gráfica oferece suporte há algo não suportado por ela, ou (b) é um bug de driver. Se ainda não funcionar com o dispositivo REF, trata-se de um bug de aplicativo.

## <a name="hardware-vs-software-vertex-processing"></a>Processamento de vértice de software versus hardware

O processamento de vértice de hardware versus software se aplica somente aos dispositivos HAL. Quando você transmite os vértices por push através do pipeline, eles precisam ser transformadas (pelas matrizes de mundo, modo de exibição e projeção) e iluminados (pelas internas luzes do D3D) - esse estágio de processamento é conhecido como T&L (para transformação e iluminação). O processamento de vértice de hardware significa que isso é feito no hardware, se o hardware oferecer suporte a ele; logo, o processamento de vértice de software é feito no software. A prática geral é a criação de um dispositivo de Hardware T&L primeiro, se isso falhar, tente Misto e se falhar novamente tente Software. (Se o software falhar, desistir e sair com um erro).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
