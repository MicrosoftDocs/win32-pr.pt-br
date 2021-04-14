---
title: Nomes de dispositivo
description: Nomes de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453727"
---
# <a name="device-names"></a>Nomes de dispositivo

Para cada tipo de dispositivo, pode haver vários drivers MCI que compartilham o conjunto de comandos, mas operam em formatos de dados diferentes. Para identificar exclusivamente um driver MCI, o MCI usa *nomes de dispositivo*.

Os nomes de dispositivo são identificados na \[ \] seção MCI do arquivo SYSTEM.INI ou na parte apropriada do registro. Essas informações identificam todos os drivers MCI para o Windows. As entradas na \[ seção MCI \] usam o seguinte formato:

*\_ nome do dispositivo* driver nome do  =  *\_ arquivo. extensão*

O exemplo a seguir mostra uma \[ seção MCI típica \] da SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Se um driver MCI for instalado usando um nome de dispositivo que já existe no SYSTEM.INI ou no registro, o sistema acrescentará um inteiro ao nome do dispositivo do novo driver, criando um nome de dispositivo exclusivo. No exemplo anterior, um driver adicional instalado usando o nome do dispositivo "cdaudio" seria atribuído ao nome do dispositivo "cdaudio1".

 

 




