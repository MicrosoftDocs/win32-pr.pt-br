---
title: Método ConvertLicenses da classe Win32_TSLicenseKeyPack classe
description: Converte as licenças no pacote de chaves atual.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Método ConvertLicenses Serviços de Área de Trabalho Remota
- Método ConvertLicenses Serviços de Área de Trabalho Remota , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Serviços de Área de Trabalho Remota método , ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfb65ea7429af14e633c8dee655b4977427e3a685e1404856fd9b5f2daf2ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099566"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Método ConvertLicenses da classe \_ Win32 TSLicenseKeyPack

Converte as licenças no pacote de chaves atual. Se a licença for uma licença por usuário, ela será convertida em uma licença por dispositivo. Se a licença for uma licença por dispositivo, ela será convertida em uma licença por usuário.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contagem* \[ Em\]
</dt> <dd>

O número de licenças a serem convertidas.

</dd> <dt>

*KeypackID* \[ out\]
</dt> <dd>

O identificador do pacote de chaves resultante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





