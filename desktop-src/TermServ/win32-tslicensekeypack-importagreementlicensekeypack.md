---
title: Método ImportAgreementLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportAgreementLicenseKeyPack
- Método ImportAgreementLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportAgreementLicenseKeyPack
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
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086354"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportAgreementLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.

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

*Agreementtype* \[ no\]
</dt> <dd>

Tipo de contrato.

<dt>

0
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença de volume selecionado (para clientes com 250 ou mais computadores). O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

1
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença de volume corporativo para clientes com 250 ou mais computadores. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

2
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença por volume de campus para uma instituição de ensino superior. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

3
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença por volume da escola para instituições primárias e secundárias. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

4
</dt> <dd>

O pacote de chaves de licença é de um contrato de licença de provedor de serviços para provedores de serviços para licenciar softwares da Microsoft mensalmente. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.

</dd> <dt>

5
</dt> <dd>

O pacote de chaves de licença é de outro contrato de licença, como valor aberto, licença aberta de vários anos e licença de assinatura aberta. O parâmetro *sAgreementNumber* é o número do contrato fornecido com as informações do programa.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ no\]
</dt> <dd>

Número do contrato ou número de registro. O parâmetro *sAgreementNumber* é uma cadeia de caracteres numérica de sete dígitos sem hifens.

</dd> <dt>

*ProductVersion* \[ no\]
</dt> <dd>

Versão do produto.

<dt>

0
</dt> <dd>

Não há suporte.

</dd> <dt>

1
</dt> <dd>

Não há suporte.

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

Número de licenças a serem importadas.

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

 

 





