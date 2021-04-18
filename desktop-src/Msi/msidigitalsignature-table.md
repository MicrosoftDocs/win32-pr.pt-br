---
description: A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabela MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750230"
---
# <a name="msidigitalsignature-table"></a>Tabela MsiDigitalSignature

A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.

As tabelas MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) estão disponíveis a partir da versão Windows Installer 2,0.

Windows Installer versão pode usar assinaturas digitais como um meio de detectar recursos corrompidos. Windows Installer 2,0 só pode verificar as assinaturas digitais de gabinetes externos e somente pelo uso das tabelas MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) .

A partir do Windows Installer 3,0, o Windows Installer pode verificar as assinaturas digitais de patches (arquivos. msp) usando as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Para obter mais informações, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [aplicação de patches de UAC (controle de conta de usuário)](user-account-control--uac--patching.md).

A tabela MsiDigitalSignature tem as colunas a seguir.



| Coluna               | Tipo                         | Chave | Nullable |
|----------------------|------------------------------|-----|----------|
| Tabela                | [Identificador](identifier.md) | S   | N        |
| Signobject           | [Text](text.md)             | S   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |
| Hash                 | [Binary](binary.md)         | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Com a versão Windows Installer 2,0, a entrada nesse campo deve ser "Media" para a [tabela de mídia](media-table.md). O instalador só verifica as assinaturas digitais em entradas de mídia de gabinete externo. Essa coluna e a coluna Signobject, juntas, especificam o recurso assinado digitalmente.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>Signobject
</dt> <dd>

Uma chave estrangeira na chave primária da tabela especificada pela coluna da tabela. Essa coluna e a coluna da tabela juntas especificam o recurso assinado digitalmente.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Uma chave estrangeira na [tabela MsiDigitalCertificate](msidigitalcertificate-table.md). Isso identifica o certificado que deve existir no arquivo para que a ação associada seja realizada com sucesso. O recurso (ou objeto) sempre é necessário para corresponder a esse certificado na tabela MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Tralha
</dt> <dd>

Neste campo, insira o hash de referência do recurso (ou objeto) que deve ser verificado em relação ao hash real do recurso (ou objeto) Obtido em tempo de execução. Se apenas o certificado precisar ser verificado, o campo de hash poderá ser nulo. Observe que o formato do hash depende do tipo de recurso (ou objeto) que está sendo assinado.

A coluna de hash contém a representação binária do hash. O conteúdo real é o membro **pbData** da estrutura [**de \_ \_ blobs de hash criptd**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , que faz parte da estrutura de **\_ BLOBs do CRYPTOAPI** . Isso pode ser obtido chamando [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ou [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).

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

[Tabela MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> <dt>

[Assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
