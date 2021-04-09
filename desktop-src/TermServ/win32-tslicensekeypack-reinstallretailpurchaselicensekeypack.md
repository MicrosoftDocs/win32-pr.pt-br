---
title: Método ReinstallRetailPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallRetailPurchaseLicenseKeyPack
- Método ReinstallRetailPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008959"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallRetailPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseCode* \[ no\]
</dt> <dd>

Contém o código de licença de 25 caracteres. Somente a cadeia de caracteres alfanumérica de 25 caracteres deve ser fornecida como entrada. Nenhum hífen deve ser adicionado.

</dd> <dt>

*Pacote de chaves* \[ fora\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





