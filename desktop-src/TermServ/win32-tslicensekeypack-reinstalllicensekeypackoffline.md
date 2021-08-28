---
title: Método ReinstallLicenseKeyPackOffline da classe Win32_TSLicenseKeyPack
description: Reinstala um Serviços de Área de Trabalho Remota de chaves de licença que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Método ReinstallLicenseKeyPackOffline Serviços de Área de Trabalho Remota
- Método ReinstallLicenseKeyPackOffline Serviços de Área de Trabalho Remota , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Serviços de Área de Trabalho Remota , método ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b72ad2175e0d97cba5733461431726781aebc9a53c1a23f408f7d14e75dd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058324"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallLicenseKeyPackOffline da classe \_ TSLicenseKeyPack do Win32

Reinstala um Serviços de Área de Trabalho Remota de chaves de licença que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseKeyPackId* \[ Em\]
</dt> <dd>

Contém o código de licença de 35 caracteres. Somente a cadeia de caracteres alfanuméricos de 35 caracteres deve ser dada como entrada. Nenhum hífen deve ser adicionado.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





