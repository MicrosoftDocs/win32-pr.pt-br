---
description: O Windows instalador pode usar assinaturas digitais para detectar recursos corrompidos.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Assinaturas digitais e Windows Instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692806"
---
# <a name="digital-signatures-and-windows-installer"></a>Assinaturas digitais e Windows Instalador

O Windows instalador pode usar assinaturas digitais para detectar recursos corrompidos. Um certificado de signante pode ser comparado com o certificado de signante de um recurso externo a ser instalado pelo pacote. Para obter mais informações sobre o uso de assinaturas digitais, certificados [](https://msdn.microsoft.com/library/cc527452.aspx) digitais e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte a seção Segurança do Microsoft Windows Software Development Kit (SDK).

Com Windows Instalador, as assinaturas digitais podem ser usadas com pacotes do instalador Windows, transformaçãos, patches, módulos de mesclagem e arquivos de gabinete externos. Windows O instalador é integrado à Política de Restrição de Software no Microsoft Windows XP. As políticas podem ser criadas para permitir ou impedir instalações com base em critérios diferentes, incluindo um determinado certificado de signante ou publicador. O Windows instalador pode executar a validação de assinatura de arquivos de gabinete externos em todas as plataformas em que o CryptoAPI versão 2.0 está instalado.

Observe que o exemplo Setup.exe inicialização fornecida com o SDK do Windows Installer executa uma verificação de assinatura em um pacote do Windows Installer antes de iniciar a instalação.

Executar uma [instalação administrativa](administrative-installation.md) remove a assinatura digital do pacote. Uma instalação administrativa modifica o pacote de instalação para adicionar o fluxo AdminProperties, o que invalidaria a assinatura digital original. Um administrador pode abandonar o pacote.

Aplicar um patch a uma instalação administrativa também remove a assinatura digital do pacote. O motivo é que as alterações persistem no pacote de instalação com patch da instalação administrativa. Um administrador pode abandonar o pacote.

A partir do Windows Installer versão 3.0, a Aplicação de Patch do [UAC (Controle](user-account-control--uac--patching.md) de Conta de Usuário) permite que usuários não administradores a patch de aplicativos instalados no contexto por computador. A adoção de patch UAC é habilitada fornecendo um certificado de signante na tabela [MsiPatchCertificate](msipatchcertificate-table.md) e assinando patches com o mesmo certificado.

Para obter mais informações, consulte Assinaturas digitais e arquivos de gabinete [](authoring-a-fully-verified-signed-installation.md) [externos,](digital-signatures-and-external-cabinet-files.md)política de instalação [](a-url-based-windows-installer-installation-example.md)do Windows e restrição de [software,](windows-installer-and-software-restriction-policy.md)Como autor de uma instalação assinada totalmente verificada e Exemplo de instalação do instalador de url Windows.

 

 
