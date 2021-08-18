---
description: Você pode optar por um computador no serviço Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In para Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d034f0b224d8170a52ce359589693c601cb9598d716e9663493e8ac99edf2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994267"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In para Microsoft Update

Você pode optar por um computador no serviço Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.

O exemplo de script neste tópico mostra como usar o WUA (Windows Update Agent) para registrar o serviço Microsoft Update com Atualizações Automáticas. Como alternativa, para registrar o serviço, o usuário pode visitar Microsoft Update.

Antes de tentar executar este exemplo, verifique se a versão do WUA instalada no computador é a versão 7.0.6000 ou posterior. Para obter mais informações sobre como determinar a versão do WUA instalada, consulte Determinando a [versão atual do WUA.](determining-the-current-version-of-wua.md)

## <a name="example"></a>Exemplo

O exemplo de script a seguir mostra como usar o WUA (agente de atualização Windows) para registrar o serviço Microsoft Update com Atualizações Automáticas. O exemplo permite processamento adiado ou offline, se necessário.

> [!IMPORTANT]
> Esse script destina-se a demonstrar o uso das APIs Windows Update Agent e fornecer um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas. Esse script não se destina ao código de produção e o próprio script não tem suporte da Microsoft (embora as APIs do Agente de Atualização Windows subjacentes sejam suportadas).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



Em versões anteriores do WUA (uma versão mínima do WUA de 7.0.6000), você pode simplificar o processo de aceitação usando uma configuração do Registro. Depois que a chave e os valores do Registro são configurados, o Microsoft Update processo de aceitação ocorre na próxima vez que o WUA executar uma pesquisa. O processo de aceitação pode ser disparado por Atualizações Automáticas ou por um chamador de API.

Por exemplo, o caminho completo da chave e dos valores do Registro a ser definido para o processo de aceitação é o seguinte:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsUpdate** \\ **PendingServiceRegistration** \\ **7971f918-a847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = My App

**RegisterWithAU** = 1

> [!Note]
>
> A chave do Registro é respeitada apenas uma vez quando o WUA é atualizado de uma versão anterior à versão 7.0.6000 para a versão 7.0.6000 ou para uma versão posterior. Recomendamos discrição ao sobrescrever valores existentes do Registro, pois a substituição dos valores pode alterar o resultado de uma solicitação de registro de serviço anterior.
>
> A criação dessa chave do Registro requer credenciais administrativas. Por Windows Vista, o chamador deve criar a chave do Registro em um processo elevado.

 

 

 



