---
description: Aplicativos cliente que chamam interfaces WMI podem controlar os níveis de segurança de seus processos.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Definindo a segurança do processo do aplicativo cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bfa0a42390ffa433cff01300b0976d40553665c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170377"
---
# <a name="setting-client-application-process-security"></a>Definindo a segurança do processo do aplicativo cliente

Aplicativos cliente que chamam interfaces WMI podem controlar os níveis de segurança de seus processos. Todos os aplicativos WMI acessam o WMI por meio do COM e você pode chamar a função de COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança para seus processos. Os aplicativos que fazem chamadas assíncronas para o WMI e os aplicativos que se registram como consumidores de eventos definem níveis de segurança na chamada no WMI.

Se você não fizer uma chamada explícita para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), o com as chamará implicitamente com valores do registro. No entanto, os valores do registro podem ter configurações mais baixas para representação e autenticação que não fornecem a segurança necessária para o WMI. Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).

O acesso assíncrono ao WMI não é recomendado. Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use semisynchronous ou comunicação síncrona ou execute as verificações de acesso apropriadas no aplicativo cliente. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Chamadas para qualquer um dos proxies WMI ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)ou [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) usam um ponteiro fora do processo. Para obter mais informações sobre os padrões e as recomendações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

O procedimento a seguir descreve as etapas que você deve executar para definir a segurança para o WMI em seu processo de aplicativo.

**Para definir a segurança para o WMI em seu processo de aplicativo**

1.  Determine os níveis de segurança necessários para os sistemas operacionais Windows nos quais seu aplicativo cliente é executado.
2.  Chame a função COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança padrão para o processo no qual o aplicativo cliente é executado. Isso declara a quantidade de segurança que outros aplicativos exigem para acessar o processo no qual seu aplicativo é executado.
3.  Se você precisar alterar a segurança em um proxy individual, por exemplo, em outra chamada para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), chame [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Se você precisar controlar o hardware remoto ou um objeto do sistema que requer mais privilégios, use a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar os privilégios necessários. Observe que você não pode habilitar um privilégio que o processo ainda não tenha sido atribuído a ele. Para obter mais informações, consulte [verificando o acesso a objetos privados](/windows/desktop/SecAuthZ/checking-access-to-private-objects).

Para obter mais informações sobre como definir o nível de segurança do processo padrão, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md) e [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
