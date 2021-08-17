---
description: Aplicativos cliente que chamam interfaces WMI podem controlar os níveis de segurança de seus processos.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Definindo a segurança do processo de aplicativo cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739460"
---
# <a name="setting-client-application-process-security"></a>Definindo a segurança do processo de aplicativo cliente

Aplicativos cliente que chamam interfaces WMI podem controlar os níveis de segurança de seus processos. Todos os aplicativos WMI acessam o WMI por meio de COM e você pode chamar a função COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança para seus processos. Aplicativos que fazem chamadas assíncronas para WMI e aplicativos que se registram como consumidores de eventos configuram níveis de segurança na chamada para WMI.

Se você não fizer uma chamada explícita para [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)COM a chamará implicitamente com valores do Registro. No entanto, os valores do Registro podem ter configurações inferiores para representação e autenticação que não fornecem a segurança necessária para o WMI. Para obter mais informações, consulte [Definindo o nível de segurança do processo padrão usando C++.](setting-the-default-process-security-level-using-c-.md)

O acesso assíncrono ao WMI não é recomendado. Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use comunicação síncrona ou síncrona ou execute verificações de acesso adequadas em seu aplicativo cliente. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Chamadas para qualquer um dos proxies WMI ([**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)ou [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) usam um ponteiro fora do processo. Para obter mais informações sobre os padrões e recomendações, consulte Definindo a segurança em [IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

O procedimento a seguir descreve as etapas que você deve executar para definir a segurança do WMI no processo do aplicativo.

**Para definir a segurança do WMI no processo do aplicativo**

1.  Determine os níveis de segurança necessários para os Windows operacionais nos quais o aplicativo cliente é executado.
2.  Chame a função [**COInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) COM para definir a segurança padrão para o processo no qual o aplicativo cliente é executado. Isso declara a segurança que outros aplicativos exigem para acessar o processo no qual seu aplicativo é executado.
3.  Se você precisar alterar a segurança em um proxy individual, por exemplo, em outra chamada para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), chame [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Se você precisar controlar o hardware remoto ou um objeto do sistema que exija mais privilégios, use a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar os privilégios necessários. Observe que você não pode habilitar um privilégio que o processo ainda não atribuiu a ele. Para obter mais informações, consulte [Verificando o acesso a objetos privados.](/windows/desktop/SecAuthZ/checking-access-to-private-objects)

Para obter mais informações sobre como definir o nível de segurança do processo padrão, consulte Definindo o nível de segurança do processo padrão usando [C++](setting-the-default-process-security-level-using-c-.md) e Definindo o nível de segurança de processo padrão [usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
