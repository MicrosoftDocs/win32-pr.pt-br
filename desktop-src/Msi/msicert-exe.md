---
description: Windows Installer pode usar assinaturas digitais como um meio de detectar recursos corrompidos.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172022"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Installer pode usar assinaturas digitais como um meio de detectar recursos corrompidos. Um certificado de signatário pode ser comparado ao certificado de assinante de um recurso externo a ser instalado pelo pacote. Para obter mais informações, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe é um utilitário de linha de comando que pode ser usado para popular a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md) com as informações de assinatura digital de um arquivo de gabinete externo. O arquivo de gabinete deve ser assinado digitalmente e listado na [tabela de mídia](media-table.md). MsiCert.exe usa as informações do certificado de signatário do gabinete assinado digitalmente e criará e adicionará as tabelas MsiDigitalSignature e MsiDigitalCertificate ao banco de dados, se elas ainda não existirem.

## <a name="syntax"></a>Syntax

**msicert-d** *{Database}* **-m** *{entrada de mídia}* **-c** *{Cabinet}* **\[ - \] h**

## <a name="command-line-options"></a>Opções de linha de comando

As opções de linha de comando não diferenciam maiúsculas de minúsculas e os delimitadores de barra podem ser usados em vez de um traço.



| Opção | Parâmetro        | Descrição                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | O banco de dados (arquivo. msi) que está sendo atualizado.                                                         |
| -M     | <media Id> | A entrada no campo DiskId da tabela de [mídia](media-table.md) no registro do arquivo de gabinete. |
| -c     | <cabinet>  | O caminho para o arquivo de gabinete assinado digitalmente.                                                          |
| -H     |                  | Inclua o hash da assinatura digital. Isso é opcional.                                            |



 

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



