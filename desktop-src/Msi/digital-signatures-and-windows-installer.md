---
description: O Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Assinaturas digitais e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758958"
---
# <a name="digital-signatures-and-windows-installer"></a>Assinaturas digitais e Windows Installer

O Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos. Um certificado de signatário pode ser comparado ao certificado de assinante de um recurso externo a ser instalado pelo pacote. Para obter mais informações sobre o uso de assinaturas digitais, certificados digitais e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte a seção [segurança](https://msdn.microsoft.com/library/cc527452.aspx) do SDK (Software Development Kit) do Microsoft Windows.

Com o Windows Installer, as assinaturas digitais podem ser usadas com Windows Installer pacotes, transformações, patches, módulos de mesclagem e arquivos de gabinete externo. O Windows Installer é integrado à diretiva de restrição de software no Microsoft Windows XP. As políticas podem ser criadas para permitir ou impedir instalações com base em critérios diferentes, incluindo um determinado certificado de signatário ou Publicador. O Windows Installer pode executar a validação de assinatura de arquivos de gabinete externo em todas as plataformas em que a versão do CryptoAPI 2,0 está instalada.

Observe que o exemplo de inicialização Setup.exe fornecido com o SDK do Windows Installer executa uma verificação de assinatura em um pacote Windows Installer antes de iniciar a instalação.

A execução de uma [instalação administrativa](administrative-installation.md) remove a assinatura digital do pacote. Uma instalação administrativa modifica o pacote de instalação do para adicionar o fluxo Adminproperties, que invalidaria a assinatura digital original. Um administrador pode desistir do pacote.

Aplicar um patch a uma instalação administrativa também remove a assinatura digital do pacote. O motivo é que as alterações persistem no pacote de instalação com patches da instalação administrativa. Um administrador pode desistir do pacote.

A partir do Windows Installer versão 3,0, a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md) permite que usuários não administradores corrijam aplicativos instalados no contexto por máquina. A aplicação de patches do UAC é habilitada fornecendo um certificado de signatário na tabela [MsiPatchCertificate](msipatchcertificate-table.md) e patches de assinatura com o mesmo certificado.

Para obter mais informações, consulte [assinaturas digitais e arquivos de gabinete externo](digital-signatures-and-external-cabinet-files.md), [Windows Installer e diretiva de restrição de software](windows-installer-and-software-restriction-policy.md), [criação de uma instalação assinada totalmente verificada](authoring-a-fully-verified-signed-installation.md)e [um exemplo de instalação de Windows Installer com base em URL](a-url-based-windows-installer-installation-example.md).

 

 
