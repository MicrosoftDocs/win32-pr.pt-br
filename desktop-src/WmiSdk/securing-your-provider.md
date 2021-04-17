---
description: Escrever um provedor seguro requer considerar como o provedor é hospedado, como o provedor lida com a representação e garantindo que os usuários sejam verificados quanto aos direitos de acesso aos dados.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protegendo seu provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782751"
---
# <a name="securing-your-provider"></a>Protegendo seu provedor

Escrever um provedor seguro requer considerar como o provedor é hospedado, como o provedor lida com a representação e garantindo que os usuários sejam verificados quanto aos direitos de acesso aos dados. Você pode proteger os dados no namespace do provedor exigindo que os dados sejam autenticados antes de enviá-los por uma rede. Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Se um usuário tiver acesso de **\_ gravação total** em qualquer namespace, o usuário poderá criar assinaturas de namespace cruzado para dados em um namespace no qual o usuário é restrito. Como um provedor pode ser carregado em qualquer namespace e ser executado em qualquer contexto de segurança, o provedor deve executar suas próprias verificações de acesso para garantir que somente usuários autorizados tenham permissão de acesso a dados ou executem métodos. Para obter mais informações, consulte [executando verificações de acesso](performing-access-checks.md).

Os tópicos a seguir abordam a segurança do provedor:

-   [Hospedagem e segurança de provedor](provider-hosting-and-security.md)
-   [Executando verificações de acesso](performing-access-checks.md)
-   [Chaves do registro para controlar a segurança do provedor](registry-keys-for-controlling-provider-security-.md)
-   [Acesso a namespaces WMI](access-to-wmi-namespaces.md)
-   [Representando um cliente](impersonating-a-client.md)

Os tópicos a seguir discutem como os clientes e scripts interagem com a segurança do provedor:

-   [Configurando a autenticação no WMI](setting-authentication-in-wmi.md)
-   [Conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
