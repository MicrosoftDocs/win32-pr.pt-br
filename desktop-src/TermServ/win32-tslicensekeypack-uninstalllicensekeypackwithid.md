---
title: Método UninstallLicenseKeyPackWithId da classe Win32_TSLicenseKeyPack
description: Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UninstallLicenseKeyPackWithId
- Método UninstallLicenseKeyPackWithId Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método UninstallLicenseKeyPackWithId
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
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454731"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a>Método UninstallLicenseKeyPackWithId da classe Win32 \_ TSLicenseKeyPack

Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pacote de chaves* \[ no\]
</dt> <dd>

O identificador do pacote de chaves a ser desinstalado.

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

 

 





