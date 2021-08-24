---
description: A tabela MsiDigitalCertificate armazena certificados no formato de fluxo binário e associa cada certificado a uma chave primária.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabela MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828776"
---
# <a name="msidigitalcertificate-table"></a>Tabela MsiDigitalCertificate

A tabela MsiDigitalCertificate armazena certificados no formato de fluxo binário e associa cada certificado a uma chave primária. A chave primária é usada para compartilhar certificados entre vários objetos assinados digitalmente. Um certificado digital é uma credencial que fornece um meio para verificar a identidade. para obter mais informações, consulte [certificados digitais](../seccrypto/digital-certificates.md) na seção [criptografia](../seccrypto/cryptography-portal.md) do SDK (Software Development Kit) do Microsoft Windows.

as tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate estão disponíveis a partir da versão Windows Installer 2,0.

Windows O instalador pode usar assinaturas digitais como um meio de detectar recursos corrompidos. Windows A versão 2,0 do instalador só pode verificar as assinaturas digitais de gabinetes externos e apenas pelo uso das tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate.

a partir do Windows Installer versão 3,0, o Windows Installer pode verificar as assinaturas digitais de patches (arquivos. msp) usando as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Para obter mais informações, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [aplicação de patches de UAC (controle de conta de usuário)](user-account-control--uac--patching.md).

A tabela MsiDigitalCertificate tem as colunas a seguir.



| Coluna             | Tipo                         | Chave | Nullable |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [Identificador](identifier.md) | Y   | N        |
| CertData           | [Binary](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Identifica o certificado de assinatura digital. Chave primária da tabela.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

A representação binária do certificado digital. A coluna CertData contém a matriz de bytes codificada de um contexto de certificado. Esse é o membro **pbCertEncoded** da estrutura [**de \_ contexto do certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) . O contexto do certificado pode ser obtido chamando [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)ou importando um arquivo. cer.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Tabela MsiDigitalSignature](msidigitalsignature-table.md)
</dt> <dt>

[assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
