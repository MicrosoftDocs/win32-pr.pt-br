---
description: Você pode optar por um computador no serviço de Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089932"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In Microsoft Update

Você pode optar por um computador no serviço de Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.

O exemplo de script neste tópico mostra como usar o WUA (Windows Update Agent) para registrar o serviço de Microsoft Update com o Atualizações Automáticas. Como alternativa, para registrar o serviço, o usuário pode visitar Microsoft Update.

Antes de tentar executar este exemplo, verifique se a versão do WUA que está instalada no computador é a versão 7.0.6000 ou uma versão posterior. Para obter mais informações sobre como determinar a versão do WUA que está instalada, consulte [determinando a versão atual do WUA](determining-the-current-version-of-wua.md).

## <a name="example"></a>Exemplo

O exemplo de script a seguir mostra como usar o WUA (agente de Windows Update) para registrar o serviço de Microsoft Update com o Atualizações Automáticas. O exemplo permite processamento adiado ou offline, se necessário.

> [!IMPORTANT]
> Esse script destina-se a demonstrar o uso das APIs do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas. Esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



Em versões anteriores do WUA (uma versão mínima do WUA do 7.0.6000), você pode simplificar o processo de aceitação usando uma configuração do registro. Depois que a chave e os valores do registro forem configurados, o Microsoft Update processo de aceitação ocorrerá na próxima vez que o WUA executar uma pesquisa. O processo de aceitação pode ser disparado por Atualizações Automáticas ou por um chamador de API.

Por exemplo, o caminho completo da chave do registro e os valores a serem definidos para o processo de aceitação são os seguintes:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = meu aplicativo

**RegisterWithAU** = 1

> [!Note]
>
> A chave do registro é respeitada apenas quando o WUA é atualizado de uma versão anterior à versão 7.0.6000 para a versão 7.0.6000 ou para uma versão posterior. Recomendamos critério ao substituir valores de registro existentes, pois substituir os valores pode alterar o resultado de uma solicitação de registro de serviço anterior.
>
> A criação dessa chave do registro requer credenciais administrativas. Para o Windows Vista, o chamador deve criar a chave do registro em um processo elevado.

 

 

 



