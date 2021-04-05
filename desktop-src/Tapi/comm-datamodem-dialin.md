---
description: comm/datamodea/conexão
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: comm/datamodea/conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922217"
---
# <a name="commdatamodemdialin"></a>comm/datamodea/conexão

A classe de dispositivo **comm/DataModel/dialem** consiste em dispositivos datamoden usados somente para chamadas de entrada. Essa classe substitui a classe [**comm/datamodea**](comm-datamodem.md) no Windows 2000 e sistemas operacionais posteriores.

Antes do Windows 2000, o Unimodem TSP só tem suporte na classe de dispositivo [**comm/DataModel**](comm-datamodem.md) . Um comportamento inesperado pode ocorrer quando um aplicativo discando uma chamada de saída altera o conjunto de configurações por um serviço aguardando uma chamada de entrada. Os aplicativos que usam o Windows 2000 e sistemas operacionais posteriores devem especificar o **comm/datamodeer/dialem** ou o [**comm/datamode/Dialer**](comm-datamodem-dialout.md) em chamadas para [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) ou [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Isso permite que o Unimodem mantenha uma configuração de conexão independente da configuração de discagem.

Embora o **comm/DataModel/dialm** seja usado pelo Unimodem no Windows 2000 e posterior, ele também pode ser usado por outros TSPs em qualquer plataforma. Os aplicativos que devem ser executados em todas as plataformas devem primeiro usar o **comm/datamodea/Dialer** em chamadas para APIs que exigem uma classe de dispositivo e usar somente o [**comm/datamodeto**](comm-datamodem.md) se a API retornar **LINEERR \_ INVALCALLSTATE**.

O provedor de serviços Unimodem converte a classe de dispositivo [**comm/datamoden**](comm-datamodem.md) em chamadas para [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para o **comm/datamodeer/diale** ou o [**comm/datamode/discout**](comm-datamodem-dialout.md) da seguinte maneira:

-   Windows 2000 e posterior:
    -   Se **NULL** for especificado no parâmetro *lpszDeviceClass* na chamada de [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), o Unimodem assumirá o **comm/datamoder/Dialer**. Se o [**comm/DataModel**](comm-datamodem.md) ou a [**TAPI/line**](tapi-line.md) forem especificados na chamada para **lineConfigDialog**, o Unimodem converterá isso em [**comm/datamodeer/dialout**](comm-datamodem-dialout.md).
    -   Na chamada para [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ou [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), o [**comm/datamodeé**](comm-datamodem.md) é tratado como [**comm/datamodeer/dialout**](comm-datamodem-dialout.md). **NULL** indica uma classe de dispositivo inválida.
-   Antes do Windows 2000:
    -   Se **NULL** ou [**TAPI/line**](tapi-line.md) for especificado em [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), o Unimodem assumirá o [**comm/datamodeto**](comm-datamodem.md).

A classe **comm/datamodeer/dial** -la usa as estruturas e configurações descritas na classe de dispositivo [**comm/datamodeling**](comm-datamodem.md) .

 

 



