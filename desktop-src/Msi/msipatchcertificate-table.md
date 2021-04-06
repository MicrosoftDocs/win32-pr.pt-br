---
description: Identifica os possíveis certificados de signatário usados para assinar digitalmente patches.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabela MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011148"
---
# <a name="msipatchcertificate-table"></a>Tabela MsiPatchCertificate

A tabela MsiPatchCertificate identifica os possíveis certificados de signatário usados para assinar digitalmente patches. A tabela MsiPatchCertificate contém as informações necessárias para habilitar a [aplicação de patches de controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para um aplicativo.

A tabela MsiPatchCertificate tem as seguintes colunas:



| Coluna               | Tipo                         | Chave | Nullable |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [Identificador](identifier.md) | S   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

O identificador exclusivo para esta linha na tabela MsiPatchCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Uma chave externa na primeira coluna da [tabela MsiDigitalCertificate](msidigitalcertificate-table.md). A linha indicada na tabela MsiDigitalCertificate contém a representação binária do certificado de signatário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os patches são sempre avaliados em relação à tabela MsiPatchCertificate que é atual no momento em que o patch é aplicado. Um patch pode modificar a tabela MsiPatchCertificate adicionando ou removendo entradas. Isso permite que um patch modifique a avaliação de patches futuros que são aplicados posteriormente na sequência de aplicação de patches. Vários certificados podem existir na tabela e o patch deve corresponder a pelo menos um certificado a ser aplicado.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[Aplicação de patch de UAC (controle de conta de usuário)](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



