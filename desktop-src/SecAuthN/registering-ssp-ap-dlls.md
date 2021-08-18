---
description: Depois de desenvolver uma biblioteca de vínculo dinâmico (SSP/PA DLL) do pacote de autenticação/provedor de suporte de segurança que contenha um ou mais pacotes de segurança personalizados, você deve registrá-lo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrando DLLs SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6405dc5ddce32ad5e4d87ed44f9344240b491fdc0ea789c30d5475ac6e73aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919496"
---
# <a name="registering-sspap-dlls"></a>Registrando DLLs SSP/AP

Depois de desenvolver uma biblioteca de vínculo dinâmico do pacote de autenticação do [*provedor de suporte de segurança*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) (SSP/AP dll) que contém um ou mais [*pacotes de segurança*](../secgloss/s-gly.md)personalizados, você deve registrá-lo. Para fazer isso, adicione o nome de sua DLL de SSP/PA personalizada aos dados do seguinte valor de registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **controlar** \\ pacotes de \\ **segurança** LSA

Os dados para esse valor de registro são uma lista dos nomes de DLLs SSP/PA, sem a extensão ".dll". O tipo de dados dessa lista é **reg \_ multi \_ sz** , portanto deve haver um caractere nulo (' \\ 0 ') entre cada nome de dll na lista.

Normalmente, as DLLs do SSP/AP são armazenadas no diretório% SystemRoot%/system32 Se esse for o caminho para sua DLL de SSP/PA personalizada, não inclua o caminho como parte do nome da DLL. Se, no entanto, a DLL estiver em um caminho diferente, inclua o caminho completo para a DLL no nome.

Cada vez que o sistema é iniciado, o LSA carrega as DLLs SSP/AP nessa lista e executa a sequência de inicialização descrita em [inicialização no modo LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registrando um pacote de segurança personalizado como o SSP padrão do TLS

Depois de desenvolver um provedor de suporte de segurança TLS personalizado e registrá-lo conforme descrito acima, você também deverá registrá-lo como o "SSP padrão do TLS". Para fazer isso, preencha o nome do pacote do seu SSP personalizado para os dados do seguinte valor de registro:

**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **controle** \\ **LSA** \\ **SSP TLS padrão**

Os dados para esse valor de registro são o nome do pacote do SSP, não o nome da dll. O tipo de dados para isso é **reg \_ sz**.

Os aplicativos de modo de usuário que usam "SSP do TLS padrão" usarão o padrão registrado aqui. Aplicativos de modo kernel ou aplicativos de modo de usuário que usam "provedor de protocolo de segurança unificada da Microsoft" ou outros nomes de SSP TLS específicos não serão afetados por essa alteração.

> [!Note]  
> Essas informações de registro pertencem apenas à DLL do SSP/PA. Para obter informações sobre como registrar os SSPs (provedores de suporte de segurança), consulte [gravando e instalando um provedor de suporte de segurança](writing-and-installing-a-security-support-provider.md). Para obter informações sobre as diferenças entre o SSP/AP e as DLLs do SSP, consulte [SSP/APS vs. SSPs](ssp-aps-versus-ssps.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições sobre o registro e a instalação de um pacote de segurança](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
