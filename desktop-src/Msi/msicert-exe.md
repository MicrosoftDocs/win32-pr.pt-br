---
description: Windows O instalador pode usar assinaturas digitais como um meio para detectar recursos corrompidos.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede88930cdb6cc616d8c39fb400f0c67c31eecd01d6d1a7d1832421cb394bcc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534536"
---
# <a name="msicertexe"></a>Msicert.exe

Windows O instalador pode usar assinaturas digitais como um meio para detectar recursos corrompidos. Um certificado de signante pode ser comparado com o certificado de signante de um recurso externo a ser instalado pelo pacote. Para obter mais informações, [consulte Assinaturas digitais e Windows Instalador .](digital-signatures-and-windows-installer.md)

MsiCert.exe é um utilitário de linha de comando que pode ser usado para preencher a tabela [MsiDigitalSignature](msidigitalsignature-table.md) e a tabela [MsiDigitalCertificate](msidigitalcertificate-table.md) com as informações de assinatura digital de um arquivo de gabinete externo. O arquivo de gabinete deve ser assinado digitalmente e listado na [tabela Mídia](media-table.md). MsiCert.exe usa as informações de certificado de signatário do gabinete assinado digitalmente e criará e adicionará as tabelas MsiDigitalSignature e MsiDigitalCertificate ao banco de dados, caso ainda não existam.

## <a name="syntax"></a>Syntax

**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Opções de linha de comando

As opções de linha de comando não fazem maiúsculas de minúsculas e delimitadores de barra podem ser usados em vez de um traço.



| Opção | Parâmetro        | Descrição                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | O banco de dados (.msi arquivo) que está sendo atualizado.                                                         |
| -M     | <media Id> | A entrada no campo DiskId da tabela [Media](media-table.md) no registro do arquivo de gabinete. |
| -c     | <cabinet>  | O caminho para o arquivo de gabinete assinado digitalmente.                                                          |
| -H     |                  | Inclua o hash da assinatura digital. Isso é opcional.                                            |



 

Essa ferramenta só está disponível no Windows [componentes do SDK para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



