---
title: Método ImportAgreementLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importa, de outro servidor de Área de Trabalho Remota licença, um pacote de chaves de licença do Serviços de Área de Trabalho Remota que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Método ImportAgreementLicenseKeyPack Serviços de Área de Trabalho Remota
- Método ImportAgreementLicenseKeyPack Serviços de Área de Trabalho Remota classe Win32_TSLicenseKeyPack ,
- Win32_TSLicenseKeyPack classe Serviços de Área de Trabalho Remota , método ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b911a722f4f26aaf83debcb70413cb9dad2b40d2ca12b4ad3310aee4510ca1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603799"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportAgreementLicenseKeyPack da classe \_ TSLicenseKeyPack do Win32

Importa, de outro servidor de Área de Trabalho Remota licença, um pacote de chaves de licença do Serviços de Área de Trabalho Remota que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
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

*AgreementType* \[ Em\]
</dt> <dd>

Tipo de contrato.

<dt>

0
</dt> <dd>

O pacote de chaves de licença é de um contrato selecionar licença por volume (para clientes com 250 ou mais computadores). O *parâmetro sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

1
</dt> <dd>

O pacote de chaves de licença é de um Enterprise de licença por volume para clientes com 250 ou mais computadores. O *parâmetro sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

2
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença por volume do Campus para uma instituição de ensino superior. O *parâmetro sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

3
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença por volume de estudante para instituições primárias e secundárias. O *parâmetro sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

4
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença do Provedor de Serviços para que os provedores de serviços licenciem o software microsoft mensalmente. O *parâmetro sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

5
</dt> <dd>

O pacote de chaves de licença é de outro contrato de licença, como Open Value, Multi-Year Open License e Open Subscription License. O *parâmetro sAgreementNumber* é o número do contrato fornecido com as informações do programa.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ Em\]
</dt> <dd>

Número do contrato ou número de registro. O *parâmetro sAgreementNumber* é uma cadeia de caracteres numérica de sete dígitos sem hifens.

</dd> <dt>

*ProductVersion* \[ Em\]
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

*ProductType* \[ Em\]
</dt> <dd>

Tipo de produto.

<dt>

0
</dt> <dd>

O Serviços de Área de Trabalho Remota tipo de produto do pacote de chaves de licença é por dispositivo. Portanto, cada dispositivo que se conecta ao servidor Host da Sessão RD deve ter uma licença.

</dd> <dt>

1
</dt> <dd>

O Serviços de Área de Trabalho Remota tipo de produto do pacote de chaves de licença é por usuário. Portanto, cada usuário que se conecta ao servidor Host da Sessão RD deve ter uma licença.

</dd> <dt>

2
</dt> <dd>

Esse tipo de produto não é válido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ Em\]
</dt> <dd>

Número de licenças a importar.

</dd> <dt>

*sSourceLSName* \[ Em\]
</dt> <dd>

O nome do servidor de Área de Trabalho Remota de origem. Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.

</dd> <dt>

*sSourceLSProductId* \[ Em\]
</dt> <dd>

O Área de Trabalho Remota do servidor de licença. O é uma cadeia de caracteres alfanumérico de 35 caracteres que não pode incluir hifens.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Recebe o identificador do pacote de chaves.

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

 

 





