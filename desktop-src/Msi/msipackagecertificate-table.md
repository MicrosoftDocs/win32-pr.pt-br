---
description: A Tabela MsiPackageCertificate lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa Multiple-Package instalação.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabela MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62abfa23f5e86949d6254ab89f7d70f01a8a4a8fe138a4eba114d2a45559390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944514"
---
# <a name="msipackagecertificate-table"></a>Tabela MsiPackageCertificate

A Tabela MsiPackageCertificate lista certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa [Instalação de Vários Pacotes](multiple-package-installations.md).

Use esta tabela para autor de uma [instalação de vários pacotes](multiple-package-installations.md) para um produto que contém vários Windows do Instalador. Se o primeiro pacote for assinado digitalmente e contiver uma Tabela MsiPackageCertificate especificando certificados digitais para todos os pacotes restantes no produto, o administrador só precisará aceitar o prompt UAC [*(Controle*](u-gly.md) de Conta de Usuário) exibido para o primeiro pacote. Depois de aceitar o prompt do UAC para o primeiro pacote, as funções definidas pelo usuário na [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) podem unir os pacotes restantes à instalação de vários pacotes sem exibir um prompt UAC e exigir uma resposta de administrador para cada pacote.

Se uma ou mais das funções na tabela [MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitarem um pacote não assinado, outro prompt UAC que exija interação do administrador será exibido para cada pacote não assinado. Se o administrador aceitar esse prompt de UAC, a instalação de vários pacotes continuará. Depois que um administrador tiver fornecido credenciais para um pacote, nenhum prompt UAC será exibido novamente para esse pacote durante essa instalação de vários pacotes. Se o administrador rejeitar um prompt do UAC para um pacote, o Windows instalador do Windows retornará a instalação de vários pacotes antes de se comprometer a instalar os pacotes que pertencem ao produto.

**[Windows Instalador 4.0 ou anterior:](not-supported-in-windows-installer-4-0.md)** Sem suporte. Esta tabela está disponível a partir do Windows Installer 4.5.

A Tabela MsiPackageCertificate tem as seguintes colunas:



| Coluna               | Tipo                         | Chave | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identificador](identifier.md) | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

O identificador exclusivo para essa linha na tabela MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Uma chave externa na primeira coluna da [tabela MsiDigitalCertificate](msidigitalcertificate-table.md). A linha indicada na Tabela MsiDigitalCertificate contém a representação binária do certificado de signatário.

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

 

 



