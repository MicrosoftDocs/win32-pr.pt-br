---
title: Fornecendo permissões de usuário para dispositivos de gravação de mídia
description: Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários conectados diretamente no computador (usuários intermediários).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758553"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fornecendo permissões de usuário para dispositivos de gravação de mídia

Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários conectados diretamente no computador (usuários intermediários). No entanto, Windows XP e Windows Server 2003, um administrador deve conceder esses privilégios de leitura/gravação do dispositivo a outros grupos de usuários.

Um administrador pode ajustar permissões específicas relacionadas ao dispositivo para usuários de energia e usuários interativos.

Para acessar o painel de permissões de grupo apropriado no Windows XP, clique em Iniciar **,** clique em Executar **,** digite **gpedit.msc** e clique em **OK**. Na interface Política de Grupo, expanda Configuração do **Computador,** expanda **Windows Configurações,** expanda Segurança **Configurações,** expanda Políticas Locais e clique duas vezes em Opções **de Segurança**.

![Captura de tela que mostra a janela "Política de Grupo" com uma política selecionada no painel 'Política'.](images/gpolpanel.jpg)

Neste painel, um administrador deve especificar as configurações de duas opções de dispositivo para fornecer as permissões de grupo necessárias:

-   Definir "Dispositivos: restringir o acesso de CD-ROM somente ao usuário conectado localmente" como **Habilitado**
-   De acordo com "Dispositivos: permitido formatar e ejetar mídia removível" para **Administradores e Usuários do Power.** Também é possível emular permissões Windows Vista definindo essa opção como **Administradores e Usuários Interativos.**

Embora uma interface do usuário específica não exista no Windows XP ou no Windows Server 2003 para o uso de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), é possível usar essas APIs para conceder permissões de dispositivo de grupos de usuários personalizados. Por exemplo, uma chamada para **SetSecurityInfo** concederá permissões a grupos de usuários. As alterações de permissão com essa API são temporárias e não persistirão em uma reinicialização. No entanto, [chamar SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implementará as alterações de permissão no Registro, que persistirão em uma reinicialização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando IMAPI](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 