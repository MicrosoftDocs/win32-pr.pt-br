---
description: A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabela MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18514747e5bb99f03bacc792f9a9ec311e28006b837061ce96088c3b723bf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679784"
---
# <a name="msidigitalsignature-table"></a>Tabela MsiDigitalSignature

A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.

As tabelas MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) estão disponíveis a partir do Windows Installer versão 2.0.

Windows A versão do instalador pode usar assinaturas digitais como um meio de detectar recursos corrompidos. Windows O Instalador 2.0 só pode verificar as assinaturas digitais de gabinetes externos e apenas pelo uso das tabelas MsiDigitalSignature e [MsiDigitalCertificate.](msidigitalcertificate-table.md)

A partir do Windows Installer 3.0, o instalador do Windows pode verificar as assinaturas digitais de patches (arquivos .msp) usando as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Para obter mais informações, consulte [Diretrizes para a adoção de](guidelines-for-authoring-secure-installations.md) instalações seguras e a adoção [de patch do UAC (Controle](user-account-control--uac--patching.md)de Conta de Usuário).

A tabela MsiDigitalSignature tem as seguintes colunas.



| Coluna               | Tipo                         | Chave | Nullable |
|----------------------|------------------------------|-----|----------|
| Tabela                | [Identificador](identifier.md) | Y   | N        |
| SignObject           | [Text](text.md)             | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |
| Hash                 | [Binary](binary.md)         | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Com o Windows Instalador 2.0, a entrada nesse campo deve ser "Mídia" para a [tabela Mídia](media-table.md). O instalador verifica apenas as assinaturas digitais em entradas de mídia de gabinete externas. Essa coluna e a coluna SignObject juntas especificam o recurso assinado digitalmente.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

Uma chave estrangeira na chave primária da tabela especificada pela coluna Tabela. Essa coluna e a coluna Tabela, juntas, especificam o recurso assinado digitalmente.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Uma chave estrangeira na [tabela MsiDigitalCertificate](msidigitalcertificate-table.md). Isso identifica o certificado que deve existir no arquivo para que a ação associada seja bem-sucedida. O recurso (ou objeto) é sempre necessário para corresponder a esse certificado na tabela MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash
</dt> <dd>

Nesse campo, insira o hash de referência do recurso (ou objeto) que deve ser verificado em relação ao hash real do recurso (ou objeto) obtido em tempo de executar. Se apenas o certificado precisar ser verificado, o campo Hash poderá ser nulo. Observe que o formato do hash depende do tipo do recurso (ou objeto) que está sendo assinado.

A coluna Hash contém a representação binária do hash. O conteúdo real é o **membro pbData** da estrutura [**CRYPT HASH \_ \_ BLOB,**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) que faz parte da estrutura **DE \_ BLOB CRYPTOAPI.** Isso pode ser obtido chamando [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ou [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).

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

[Assinaturas digitais e Windows Instalador](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
