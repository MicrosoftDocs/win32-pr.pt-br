---
title: Referência de driver instalável
description: Referência de driver instalável
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Multimídia do Windows, referência de driver instalável
- multimídia, referência de driver instalável
- drivers instaláveis, referência
- referência de driver instalável, sobre
- referência para drivers instaláveis, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823693"
---
# <a name="installable-driver-reference"></a>Referência de driver instalável

As funções e mensagens associadas a drivers instaláveis são agrupadas da seguinte maneira.

## <a name="loading-and-unloading-drivers"></a>Carregando e descarregando drivers

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**fechamento de DRV \_**](drv-close.md)
-   [**\_desabilitar drv**](drv-disable.md)
-   [**\_habilitar drv**](drv-enable.md)
-   [**DRV \_ Free**](drv-free.md)
-   [**carregamento de DRV \_**](drv-load.md)
-   [**DRV \_ Open**](drv-open.md)

## <a name="configuring-a-driver"></a>Configurando um driver

-   [**\_Configurar drv**](drv-configure.md)
-   [**\_QUERYCONFIGURE drv**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Instalando um driver

-   [**instalação do DRV \_**](drv-install.md)
-   [**remoção de DRV \_**](drv-remove.md)

## <a name="driver-functions"></a>Funções de driver

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> </dl>

 

 