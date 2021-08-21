---
title: Método ImportOpenPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportOpenPurchaseLicenseKeyPack
- Método ImportOpenPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768961bda04776a73d0aa74422ce0ed5088e041ee41e4732becd72914dcabf04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008466"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportOpenPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
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

O número de licenças a serem importadas

</dd> <dt>

*sSourceLSName* \[ no\]
</dt> <dd>

O nome do servidor de licença de Área de Trabalho Remota de origem. Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.

</dd> <dt>

*sSourceLSProductId* \[ no\]
</dt> <dd>

O identificador do servidor de licença Área de Trabalho Remota. O é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.

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

 

 





