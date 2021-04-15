---
description: O método FileSignatureInfo do objeto do instalador usa o caminho para um arquivo e retorna um SAFEARRAY de bytes que representam o hash ou o certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Método Installer. FileSignatureInfo
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
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747334"
---
# <a name="installerfilesignatureinfo-method"></a>Método Installer. FileSignatureInfo

O método **FileSignatureInfo** do objeto do [**instalador**](installer-object.md) usa o caminho para um arquivo e retorna um SafeArray de bytes que representam o hash ou o certificado codificado. Os valores podem então ser usados para preencher as tabelas [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalCertificate](msidigitalcertificate-table.md) .

Para obter mais informações, consulte o [**tipo de dados SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).

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

Caminho completo de um arquivo assinado digitalmente.

Ao preencher as tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate](msidigitalcertificate-table.md) , *FilePath* aponta para um gabinete assinado digitalmente. Ao preencher as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *FilePath* aponta para um patch assinado digitalmente.

</dd> <dt>

*Opções* 
</dt> <dd>

Sinalizadores de caso de erro especiais.



| Sinalizador                                                                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Com *as opções* definidas como MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** sempre retorna um erro fatal para um hash inválido. <br/> Se *as opções* não estiverem definidas como msiSignatureOptionInvalidHashFatal e o *formato* for definido como msiSignatureInfoCertificate, **FileSignatureInfo** não retornará um erro para um hash inválido.<br/> |



 

</dd> <dt>

*Formato* 
</dt> <dd>

As informações de assinatura solicitadas.



| Sinalizador                                                                                                                                                                                                                                                                                                        | Significado                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Retorna um SAFEARRAY de bytes que representa o certificado codificado.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Retorna um SAFEARRAY de bytes que representa o hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o método retornará um [SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contenham o certificado hash ou codificado.

## <a name="remarks"></a>Comentários

Para criar uma instalação assinada totalmente verificada usando a automação, use o método **FileSignatureInfo** para popular as tabelas [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature](msidigitalsignature-table.md) . Para obter mais informações, consulte [criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
