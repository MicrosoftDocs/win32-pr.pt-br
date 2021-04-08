---
description: comm/datamodea/dialout
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: comm/datamodea/dialout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922216"
---
# <a name="commdatamodemdialout"></a>comm/datamodea/dialout

A classe de dispositivo **comm/datamodeer/dialout** consiste em dispositivos datamoden usados somente para chamadas de saída. Essa classe substitui a classe [**comm/datamodea**](comm-datamodem.md) no Windows 2000 e sistemas operacionais posteriores.

Antes do Windows 2000, o Unimodem TSP só tem suporte na classe de dispositivo [**comm/DataModel**](comm-datamodem.md) . Um comportamento inesperado pode ocorrer quando um aplicativo discando uma chamada de saída altera o conjunto de configurações por um serviço aguardando uma chamada de entrada. Os aplicativos que usam o Windows 2000 e sistemas operacionais posteriores devem especificar o [**comm/datamodeer/dialem**](comm-datamodem-dialin.md) ou o **comm/datamode/Dialer** em chamadas para [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) ou [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Isso permite que o Unimodem mantenha uma configuração de conexão independente da configuração de discagem.

Embora o **comm/datamodeer/dialout** seja usado pelo Unimodem no Windows 2000 e posterior, ele também pode ser usado por outros TSPs em qualquer plataforma. Os aplicativos que devem ser executados em todas as plataformas devem primeiro usar o **comm/datamodeer/Dialer** em chamadas à API que exigem uma classe de dispositivo e usar somente o [**comm/datamodeto**](comm-datamodem.md) se a API retornar **LINEERR \_ INVALCALLSTATE**.

O provedor de serviços Unimodem converte a classe de dispositivo [**comm/datamoden**](comm-datamodem.md) em chamadas para [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para o [**comm/datamodeer/diale**](comm-datamodem-dialin.md) ou o **comm/datamode/discout** da seguinte maneira:

-   Windows 2000 e posterior:
    -   Se **NULL** for especificado no parâmetro *lpszDeviceClass* na chamada de [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), o Unimodem assumirá o [**comm/datamoder/Dialer**](comm-datamodem-dialin.md). Se o [**comm/DataModel**](comm-datamodem.md) ou a [**TAPI/line**](tapi-line.md) forem especificados na chamada para **lineConfigDialog**, o Unimodem converterá isso em **comm/datamodeer/dialout**.
    -   Na chamada para [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ou [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), o [**comm/datamodeé**](comm-datamodem.md) é tratado como **comm/datamodeer/dialout**. **NULL** indica uma classe de dispositivo inválida.
-   Antes do Windows 2000:
    -   Se **NULL** ou [**TAPI/line**](tapi-line.md) for especificado em [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), o Unimodem assumirá o [**comm/datamodeto**](comm-datamodem.md).

A classe **comm/datamodeer/dialout** usa as estruturas e configurações descritas na classe de dispositivo [**comm/datamodeling**](comm-datamodem.md) .

 

 



