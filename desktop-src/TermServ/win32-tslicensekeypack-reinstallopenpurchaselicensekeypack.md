---
title: Método ReinstallOpenPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallOpenPurchaseLicenseKeyPack
- Método ReinstallOpenPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6519e6eedc187b6db2ee93a776843b0f305430df7ae55e4356ebce4de5ad31d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137819"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallOpenPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseNumber* \[ no\]
</dt> <dd>

Cadeia de caracteres numérica de 8 caracteres fornecida com o pacote de chaves de licença. O parâmetro *sLicenseNumber* não pode conter hifens.

</dd> <dt>

*sAuthorizationNumber* \[ no\]
</dt> <dd>

Cadeia de caracteres alfanumérica de 15 caracteres que é fornecida com a chave de licença. O parâmetro *sAuthorizationNumber* não pode conter hifens.

</dd> <dt>

*ProductVersion* \[ no\]
</dt> <dd>

Versão do produto.

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

Tipo de produto.

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

O número de licenças a serem instaladas.

</dd> <dt>

*Pacote de chaves* \[ fora\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

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

 

 





