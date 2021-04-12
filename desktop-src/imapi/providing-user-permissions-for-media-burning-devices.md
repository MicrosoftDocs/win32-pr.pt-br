---
title: Fornecendo permissões de usuário para dispositivos de gravação de mídia
description: Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários registrados diretamente no computador (usuários intermediários).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104172407"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fornecendo permissões de usuário para dispositivos de gravação de mídia

Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários registrados diretamente no computador (usuários intermediários). No entanto, no Windows XP e no Windows Server 2003, um administrador deve conceder esses privilégios de leitura/gravação de dispositivo a outros grupos de usuários.

Um administrador pode ajustar permissões específicas relacionadas ao dispositivo para usuários avançados e usuários interativos.

Para acessar o painel de permissões de grupo apropriado no Windows XP, clique em **Iniciar**, **executar**, digite **gpedit. msc** e clique em **OK**. Na interface Política de Grupo, expanda **configuração do computador**, expanda **configurações do Windows**, expanda **configurações de segurança**, expanda **políticas locais** e clique duas vezes em **Opções de segurança**.

![Captura de tela que mostra a janela ' Política de Grupo ' com uma política selecionada no painel ' política '.](images/gpolpanel.jpg)

Neste painel, um administrador deve especificar as configurações de duas opções de dispositivo para fornecer as permissões de grupo necessárias:

-   Defina "dispositivos: restringir o acesso ao CD-ROM somente para o usuário conectado localmente" para **habilitado**
-   Defina "dispositivos: com permissão para formatar e ejetar mídia removível" para **Administradores e usuários avançados**. Também é possível emular permissões do Windows Vista definindo essa opção como **Administradores e usuários interativos**.

Embora uma interface do usuário específica não exista no Windows XP ou no Windows Server 2003 para o uso de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), é possível usar essas APIs para conceder permissões de dispositivo a grupos de usuários personalizados. Por exemplo, uma chamada para **SetSecurityInfo** concederá permissões a grupos de usuários. As alterações de permissão com essa API são temporárias e não serão mantidas em uma reinicialização. No entanto, chamar [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) irá implementar as alterações de permissão no registro, que persistirão em uma reinicialização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o IMAPi](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 