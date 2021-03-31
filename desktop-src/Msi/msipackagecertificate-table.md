---
description: A tabela MsiPackageCertificate lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa Multiple-Package instalação.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabela MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172020"
---
# <a name="msipackagecertificate-table"></a>Tabela MsiPackageCertificate

A tabela MsiPackageCertificate lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa [instalação de vários pacotes](multiple-package-installations.md).

Use esta tabela para criar uma [instalação de vários pacotes](multiple-package-installations.md) para um produto que contém vários pacotes de Windows Installer. Se o primeiro pacote for assinado digitalmente e contiver uma tabela MsiPackageCertificate especificando certificados digitais para todos os pacotes restantes do produto, o administrador precisará aceitar apenas o prompt do [*controle de conta de usuário*](u-gly.md) (UAC) exibido para o primeiro pacote. Depois de aceitar o prompt do UAC para o primeiro pacote, as funções definidas pelo usuário na [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) podem então unir os pacotes restantes à instalação de vários pacotes sem exibir um prompt do UAC e exigir uma resposta de administrador para cada pacote.

Se uma ou mais das funções na [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitarem um pacote não assinado, outro prompt do UAC que exigir a interação do administrador será exibido para cada pacote não assinado. Se o administrador aceitar esse prompt do UAC, a instalação de vários pacotes continuará. Depois que um administrador tiver fornecido credenciais para um pacote, nenhum prompt do UAC será exibido novamente para esse pacote durante a instalação de vários pacotes. Se o administrador rejeitar um prompt de UAC para um pacote, o Windows Installer reverterá a instalação de vários pacotes antes de confirmar a instalação de todos os pacotes pertencentes ao produto.

**[Windows Installer 4,0 ou anterior](not-supported-in-windows-installer-4-0.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 4,5.

A tabela MsiPackageCertificate tem as seguintes colunas:



| Coluna               | Tipo                         | Chave | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identificador](identifier.md) | S   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

O identificador exclusivo para esta linha na tabela MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Uma chave externa na primeira coluna da [tabela MsiDigitalCertificate](msidigitalcertificate-table.md). A linha indicada na tabela MsiDigitalCertificate contém a representação binária do certificado de signatário.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[Tabela MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> </dl>

 

 



