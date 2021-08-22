---
title: Método UninstallLicenseKeyPackWithId da classe Win32_TSLicenseKeyPack dados
description: Desinstala o Serviços de Área de Trabalho Remota de chaves de licença com o identificador do pacote de chaves especificado.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Método UninstallLicenseKeyPackWithId Serviços de Área de Trabalho Remota
- Método UninstallLicenseKeyPackWithId Serviços de Área de Trabalho Remota , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Serviços de Área de Trabalho Remota , método UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1218ce51beac9e20dd04e2a56d9075b6732d65e17689afaba5ce4d8f6669b1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008436"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a>Método UninstallLicenseKeyPackWithId da classe \_ TSLicenseKeyPack do Win32

Desinstala o Serviços de Área de Trabalho Remota de chaves de licença com o identificador do pacote de chaves especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeyPackId* \[ Em\]
</dt> <dd>

O identificador do pacote de chaves a ser desinstalado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

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

 

 





