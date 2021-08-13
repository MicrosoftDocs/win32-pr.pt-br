---
description: os autores de pacote podem monitorar mensagens Windows Installer internas por meio da criação de um aplicativo executável que contém um manipulador de retorno de chamada para receber as mensagens e a funcionalidade para iniciar uma instalação.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Monitorando uma instalação usando o MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660b1454d7e4f3437da6dce41707a1516207d853510e8475837f31e60090b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628567"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>Monitorando uma instalação usando o MsiSetExternalUI

os autores de pacote podem monitorar mensagens Windows Installer internas por meio da criação de um aplicativo executável que contém um manipulador de retorno de chamada para receber as mensagens e a funcionalidade para iniciar uma instalação.

O manipulador de retorno de chamada está em conformidade com o \_ protótipo do manipulador INSTALLUI e um ponteiro para esse manipulador de retorno de chamada é passado para [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia). Depois que a instalação for iniciada por uma chamada para [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), as mensagens de instalação serão interceptadas pelo manipulador de retorno de chamada e o autor do pacote poderá exibir ou ignorar seletivamente qualquer ou todas essas mensagens.

para obter mais informações, consulte [manipulando mensagens de progresso usando MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [retornando valores de um manipulador de Interface de usuário externo](returning-values-from-an-external-user-interface-handler.md)e [analisando Windows Installer mensagens](parsing-windows-installer-messages.md).

Para obter mais informações sobre como usar um manipulador externo baseado em registro, consulte [monitorando uma instalação usando o MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

 

 



