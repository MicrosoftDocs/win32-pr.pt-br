---
description: Visão geral do tratamento de erros ao usar as APIs (interfaces de programação de aplicativo) do StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Considerações de tratamento de erro para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920961"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Considerações de tratamento de erro para a API StylusInput

As exceções não tratadas geradas por um plug-in são capturadas pelo objeto [**RealTimeStylus**](realtimestylus-class.md) . Quando um plug-in gera uma exceção, o fluxo normal de dados é interrompido. O objeto **RealTimeStylus** :

1.  Cria um objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) (em código gerenciado).
2.  Chama o método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (em código gerenciado, o método [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) ) do plug-in que gerou a exceção.
3.  Chama o método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) dos plug-ins restantes nessa coleção.
4.  Se o plug-in que gerou a exceção for um plug-in síncrono, o objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) (em código gerenciado) será adicionado à fila de saída.
5.  O objeto [**RealTimeStylus**](realtimestylus-class.md) retoma o processamento normal dos dados originais.

Se um plug-in lançar uma exceção do seu método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , o objeto [**RealTimeStylus**](realtimestylus-class.md) capturará a exceção, mas não gerará um novo objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) . Para obter mais informações sobre como o ErrorData é adicionado à fila, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) não interrompe o processamento de dados do fluxo de dados da caneta eletrônica quando um de seus plug-ins gera uma exceção. Dependendo do seu design, alguns dos seus plug-ins talvez precisem assinar a notificação [ErrorData](/previous-versions/ms575221(v=vs.100)) e modificar seu comportamento quando ocorrer uma exceção.

 

 
