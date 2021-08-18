---
title: Referência de driver instalável
description: Referência de driver instalável
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows multimídia, referência de driver instalável
- multimídia, referência de driver instalável
- drivers instaláveis, referência
- referência de driver instalável, sobre
- referência para drivers instaláveis, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dd2488f0b07805edbcdc90187309db2a04c9c0ced4f4b5b0af4e50bd983ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038636"
---
# <a name="installable-driver-reference"></a>Referência de driver instalável

As funções e mensagens associadas a drivers instaláveis são agrupadas da seguinte forma.

## <a name="loading-and-unloading-drivers"></a>Carregando e descarregando drivers

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**DRV \_ CLOSE**](drv-close.md)
-   [**DRV \_ DISABLE**](drv-disable.md)
-   [**HABILITAR DRV \_**](drv-enable.md)
-   [**DRV \_ GRATUITO**](drv-free.md)
-   [**CARGA DE \_ DRV**](drv-load.md)
-   [**DRV \_ OPEN**](drv-open.md)

## <a name="configuring-a-driver"></a>Configurando um driver

-   [**CONFIGURAÇÃO DE \_ DRV**](drv-configure.md)
-   [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Instalando um driver

-   [**INSTALAÇÃO \_ DO DRV**](drv-install.md)
-   [**DRV \_ REMOVE**](drv-remove.md)

## <a name="driver-functions"></a>Funções do driver

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> </dl>

 

 