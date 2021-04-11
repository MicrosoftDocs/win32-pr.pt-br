---
title: Método RemoveLicensesWithIdCount da classe Win32_TSLicenseKeyPack
description: Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveLicensesWithIdCount
- Método RemoveLicensesWithIdCount Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008958"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Método RemoveLicensesWithIdCount da classe Win32 \_ TSLicenseKeyPack

Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pacote de chaves* \[ no\]
</dt> <dd>

O identificador do pacote de chaves que contém as licenças a serem removidas.

</dd> <dt>

*LicenseCount* \[ no\]
</dt> <dd>

O número de licenças a desinstalar.

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

 

 





