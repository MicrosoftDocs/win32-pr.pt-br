---
title: Fazendo backup e restaurando um servidor de Active Directory
description: Active Directory Domain Services fornecer funções para fazer backup e restaurar dados no banco de dados de diretório.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, usando, fazendo backup e restaurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640437"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Fazendo backup e restaurando um servidor de Active Directory

Active Directory Domain Services fornecer funções para fazer backup e restaurar dados no banco de dados de diretório. Esta seção descreve como [fazer backup](backing-up-an-active-directory-server.md) e [restaurar](restoring-an-active-directory-server.md) um servidor de Active Directory. Para obter mais informações sobre como fazer backup de um servidor de Active Directory usando os utilitários fornecidos nos sistemas operacionais Windows 2000 e Windows Server 2003, consulte o Resource Kit aplicável, disponível no site do Microsoft TechNet.

O backup de um servidor de Active Directory deve ser executado online e deve ser executado quando o Active Directory Domain Services estiver instalado. Os Active Directory Domain Services são criados em um banco de dados especial e exportam um conjunto de funções de backup que fornecem a interface de backup programática. O backup não oferece suporte a backups incrementais. Um aplicativo de backup é associado a uma DLL do lado do cliente local com pontos de entrada definidos em Ntdsbcli. h.

A restauração de um servidor de Active Directory é sempre executada offline.

Embora os tópicos nesta seção descrevam apenas como fazer backup e restaurar um servidor de Active Directory, lembre-se de que o Windows 2000 e os sistemas operacionais Windows Server 2003 têm vários componentes de "estado do sistema" que devem ser armazenados em backup e restaurados juntos. Esses componentes de estado do sistema consistem em:

-   Arquivos de inicialização, como NTLDR, NTDETECT, todos os arquivos protegidos por SFP e configuração do contador de desempenho
-   O controlador de Domínio do Active Directory
-   SysVol (somente controlador de domínio)
-   Servidor de certificado (somente CA)
-   Banco de dados do cluster (somente nó do cluster)
-   Registro
-   Banco de dados de registro de classe COM+

O backup do estado do sistema pode ser feito em qualquer ordem, mas a restauração do estado do sistema deve ocorrer na seguinte ordem:

1.  Restaure os arquivos de inicialização.
2.  Restaure SysVol, servidor de certificado, banco de dados de cluster e banco de dados de registro de classe COM+, conforme aplicável.
3.  Restaure o servidor de Active Directory.
4.  Restaure o registro.

Para obter mais informações sobre como fazer backup e restaurar os serviços de certificados, consulte [usando as funções de backup e restauração dos serviços de certificados](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Para obter mais informações sobre como fazer backup e restaurar Active Directory Domain Services, consulte:

-   [Considerações sobre o backup de Active Directory Domain Services](considerations-for-active-directory-domain-services-backup.md)
-   [Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
-   [Restaurando um servidor de Active Directory](restoring-an-active-directory-server.md)
-   [Funções de backup de diretório](directory-backup-functions.md)

 

 