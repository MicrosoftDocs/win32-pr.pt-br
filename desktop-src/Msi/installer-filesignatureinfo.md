---
description: O método FileSignatureInfo do objeto Installer leva o caminho para um arquivo e retorna um SAFEARRAY de bytes que representam o hash ou o certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Método Installer.FileSignatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630777"
---
# <a name="installerfilesignatureinfo-method"></a>Método Installer.FileSignatureInfo

O **método FileSignatureInfo** do objeto [**Installer**](installer-object.md) leva o caminho para um arquivo e retorna um SAFEARRAY de bytes que representam o hash ou o certificado codificado. Os valores podem ser usados para preencher as [tabelas MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalCertificate.](msidigitalcertificate-table.md)

Para obter mais informações, consulte [**SafeARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Sintaxe


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilePath* 
</dt> <dd>

Caminho completo para um arquivo assinado digitalmente.

Ao preencher as [tabelas MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate,](msidigitalcertificate-table.md) *FilePath* aponta para um gabinete assinado digitalmente. Ao preencher as [tabelas MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *FilePath* aponta para um patch assinado digitalmente.

</dd> <dt>

*Opções* 
</dt> <dd>

Sinalizadores de caso de erro especiais.



| Sinalizador                                                                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Com *Opções* definidas como msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** sempre retorna um erro fatal para um hash inválido. <br/> Se *Options* não estiver definido como msiSignatureOptionInvalidHashFatal e *Format* estiver definido como msiSignatureInfoCertificate, **FileSignatureInfo** não retornará um erro para um hash inválido.<br/> |



 

</dd> <dt>

*Formato* 
</dt> <dd>

As informações de assinatura solicitadas.



| Sinalizador                                                                                                                                                                                                                                                                                                        | Significado                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Retorna um SAFEARRAY de bytes que representam o certificado codificado.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Retorna um SAFEARRAY de bytes que representam o hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o método retornará [uma SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contém o hash ou o certificado codificado.

## <a name="remarks"></a>Comentários

Para autor de uma instalação assinada totalmente verificada usando a automação, use o método **FileSignatureInfo** para preencher as [tabelas MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature.](msidigitalsignature-table.md) Para obter mais informações, consulte [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como autor de uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Assinaturas digitais e Windows Instalador](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
