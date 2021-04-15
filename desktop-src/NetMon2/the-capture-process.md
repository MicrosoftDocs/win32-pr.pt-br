---
description: O processo de captura é o mesmo para cada uma das quatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: O processo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569186"
---
# <a name="the-capture-process"></a>O processo de captura

O processo de captura é o mesmo para cada uma das quatro interfaces NPP. Em cada caso, o processo inclui:

-   Obtendo o objeto de interface NPP a ser usado
-   Conectando-se à rede
-   Iniciando e, em seguida, parando a [ *captura*](c.md)
-   Desconectando da rede

> [!Note]  
> Ao obter o objeto de interface que você deseja, certifique-se de chamar apenas os métodos incluídos nessa interface. A ilustração a seguir mostra que cada interface fornece métodos semelhantes para capturar dados de rede. Um erro será retornado se você se conectar à rede com uma interface e, em seguida, tentar executar uma captura usando os métodos de outra interface.

 

As ilustrações a seguir mostram duas maneiras diferentes de executar uma captura. A primeira ilustração mostra como executar uma ou mais capturas sequenciais, permitindo que você crie qualquer número de capturas independentes.

![captura sequencial](images/capt1.png)

Conforme mostrado acima, depois de se conectar à rede, você pode iniciar e parar uma captura quantas vezes desejar, iniciando uma nova captura e gerando novas estatísticas toda vez que reiniciar a captura. Por exemplo, para uma captura atrasada usando a interface [**IDelaydC**](idelaydc.md) , um novo [*arquivo de captura*](c.md) será criado cada vez que a captura for reiniciada.

No entanto, também esteja ciente de que sempre que reiniciar o processo de captura, você deverá chamar o método configure apropriado para reconfigurar a conexão. Para a chamada inicial para iniciar a captura, a conexão é configurada pela chamada para conectar-se à rede.

A segunda ilustração mostra como você pode executar uma única captura Pausando e reiniciando.

![captura única Pausando e reiniciando](images/capt2.png)

Nesse caso, você pode pausar e reiniciar uma captura quantas vezes desejar. Com essa abordagem, você pode executar uma captura cujos dados (e suas estatísticas relacionadas) são registrados como uma única captura. Por exemplo, para executar uma captura atrasada usando a interface [**IDelaydC**](idelaydc.md) , todas as informações de rede capturadas seriam salvas em um único [*arquivo de captura*](c.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC:: configurar**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: retomar**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: iniciar**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP:: configurar**](iesp-configure.md)
</dt> <dt>

[**IESP:: conectar**](iesp-connect.md)
</dt> <dt>

[**IESP::D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: retomar**](iesp-resume.md)
</dt> <dt>

[**IESP:: iniciar**](iesp-start.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC:: configurar**](irtc-configure.md)
</dt> <dt>

[**IRTC:: conectar**](irtc-connect.md)
</dt> <dt>

[**IRTC::D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC:: retomar**](irtc-resume.md)
</dt> <dt>

[**IRTC:: iniciar**](irtc-start.md)
</dt> <dt>

[**IRTC:: Stop**](irtc-stop.md)
</dt> <dt>

[**IStats:: configurar**](istats-configure.md)
</dt> <dt>

[**IStats:: conectar**](istats-connect.md)
</dt> <dt>

[**IStats::D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats:: retomar**](istats-resume.md)
</dt> <dt>

[**IStats:: iniciar**](istats-start.md)
</dt> <dt>

[**IStats:: Stop**](istats-stop.md)
</dt> </dl>

 

 



