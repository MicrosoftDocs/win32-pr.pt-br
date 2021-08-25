---
description: O processo de captura é o mesmo para cada uma das quatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: O processo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6d82d721f0f85c6b1ab279d556aaad866f70fde7c8e422995cba5be513d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889576"
---
# <a name="the-capture-process"></a>O processo de captura

O processo de captura é o mesmo para cada uma das quatro interfaces NPP. Em cada caso, o processo inclui:

-   Obtendo o objeto de interface NPP a ser usado
-   Conectando-se à rede
-   Iniciando e, em seguida, interrompendo a [ *captura*](c.md)
-   Desconectando-se da rede

> [!Note]  
> Ao obter o objeto de interface que você deseja, certifique-se de chamar apenas os métodos incluídos nessa interface. A ilustração a seguir mostra que cada interface fornece métodos semelhantes para capturar dados de rede. Um erro será retornado se você se conectar à rede com uma interface e, em seguida, tentar executar uma captura usando os métodos de outra interface.

 

As ilustrações a seguir mostram duas maneiras diferentes de executar uma captura. A primeira ilustração mostra como executar uma ou mais capturas sequenciais, permitindo que você crie qualquer número de capturas independentes.

![captura sequencial](images/capt1.png)

Conforme mostrado acima, depois de se conectar à rede, você pode iniciar e parar uma captura quantas vezes desejar, iniciando uma nova captura e gerando novas estatísticas sempre que reiniciar a captura. Por exemplo, para uma captura atrasada usando a interface [](c.md) [**IDelaydC,**](idelaydc.md) um novo arquivo de captura será criado sempre que você reiniciar a captura.

No entanto, também esteja ciente de que sempre que você reiniciar o processo de captura, deverá chamar o método de configuração apropriado para reconfigurar a conexão. Para a chamada inicial para iniciar a captura, a conexão é configurada pela chamada para se conectar à rede.

A segunda ilustração mostra como você pode executar uma única captura pausando e reiniciando.

![captura única pausando e reiniciando](images/capt2.png)

Nesse caso, você pode pausar e reiniciar uma captura quantas vezes quiser. Com essa abordagem, você pode executar uma captura cujos dados (e suas estatísticas relacionadas) são registrados como uma única captura. Por exemplo, para executar uma captura atrasada usando a interface [**IDelaydC,**](idelaydc.md) todas as informações de rede capturadas seriam salvas em um único arquivo [*de captura*](c.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Conexão**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D conectar**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> <dt>

[**IRIA::Configure**](iesp-configure.md)
</dt> <dt>

[**I LTD::Conexão**](iesp-connect.md)
</dt> <dt>

[**I LTD::D conectar**](iesp-disconnect.md)
</dt> <dt>

[**I LTD::P ause**](iesp-pause.md)
</dt> <dt>

[**I LTD::Resume**](iesp-resume.md)
</dt> <dt>

[**I LTD::Start**](iesp-start.md)
</dt> <dt>

[**IRIA::Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC::Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC::Conexão**](irtc-connect.md)
</dt> <dt>

[**IRTC::D conectar**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC::Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC::Start**](irtc-start.md)
</dt> <dt>

[**IRTC::Stop**](irtc-stop.md)
</dt> <dt>

[**IStats::Configure**](istats-configure.md)
</dt> <dt>

[**IStats::Conexão**](istats-connect.md)
</dt> <dt>

[**IStats::D conectar**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats::Resume**](istats-resume.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 



