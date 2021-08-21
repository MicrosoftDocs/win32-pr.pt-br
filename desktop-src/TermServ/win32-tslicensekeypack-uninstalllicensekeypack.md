---
title: Método UninstallLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UninstallLicenseKeyPack
- Método UninstallLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb02ff8ecc84c346bef404071e8abb3988c0e7c8e70b54b288524e8ef790d5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348617"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método UninstallLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProductVersion* \[ no\]
</dt> <dd>

Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.

<dt>

0
</dt> <dd>

Sem suporte.

</dd> <dt>

1
</dt> <dd>

Sem suporte.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ no\]
</dt> <dd>

Tipo de produto do Serviços de Área de Trabalho Remota pacote de chaves de licença.

<dt>

0
</dt> <dd>

O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo. Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.

</dd> <dt>

1
</dt> <dd>

O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário. Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.

</dd> <dt>

2
</dt> <dd>

Este tipo de produto não é válido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ no\]
</dt> <dd>

O número de licenças a desinstalar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





