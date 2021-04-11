---
title: Difxapi.h
description: Esta seção contém tópicos de referência para o cabeçalho difxapi. h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c549ed3fd781d9fde4e6ab48703e1df425986d0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162314"
---
# <a name="difxapih"></a>Difxapi.h

Esta seção contém tópicos de referência para o cabeçalho difxapi. h.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Uma função de tipo **DIFLOGCALLBACK** é uma função de retorno de chamada fornecida pelo aplicativo que um aplicativo registra chamando [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback). DIFxAPI chama a função de retorno de chamada para registrar eventos que ocorrem durante a operação DIFxAPI.<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Uma função de tipo **DIFXAPILOGCALLBACK** é uma função de retorno de chamada fornecida pelo aplicativo que um aplicativo registra com DIFxAPI chamando [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback). DIFxAPI chama a função de retorno de chamada para registrar eventos que ocorrem durante a operação DIFxAPI.<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | A função **DIFXAPISetLogCallback** registra uma função de retorno de chamada fornecida pelo chamador que DIFxAPI chama para registrar em log informações sobre eventos que ocorrem durante operações de DIFxAPI. <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | A função **DriverPackageGetPath** recupera o caminho totalmente qualificado do [arquivo inf](/windows-hardware/drivers/install/overview-of-inf-files) para um pacote de [Driver](/windows-hardware/drivers/install/driver-packages)pré-instalado.<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | A função **DriverPackageInstall** pré-instala um pacote de [Driver](/windows-hardware/drivers/install/driver-packages) e instala o driver no sistema.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | A função **DriverPackagePreinstall** pré-instala um pacote de [Driver](/windows-hardware/drivers/install/driver-packages) para um [Driver de função](/windows-hardware/drivers/kernel/function-drivers) plug and Play (PnP) e instala o [arquivo inf](/windows-hardware/drivers/install/overview-of-inf-files) para o pacote de driver no diretório de arquivos INF do sistema.<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | A função **DriverPackageUninstall** desinstala o [pacote de driver](/windows-hardware/drivers/install/driver-packages) especificado do sistema e remove o pacote de driver. <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | A estrutura INSTALLERINFO contém informações sobre um aplicativo que o DIFxAPI associa a um [pacote de driver](/windows-hardware/drivers/install/driver-packages). <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | A função **SetDifxLogCallback** registra uma função de retorno de chamada fornecida pelo chamador que DIFxAPI chama para registrar em log informações sobre eventos que ocorrem durante operações de DIFxAPI. <br/>                                                                                                               |



 

 

 

[Enviar comentários sobre este tópico para a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Enviar comentários sobre este tópico para a Microsoft")