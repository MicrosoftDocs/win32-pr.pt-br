---
title: Método InstallAgreementLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallAgreementLicenseKeyPack
- Método InstallAgreementLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759936"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método InstallAgreementLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.

## <a name="syntax"></a>Sintaxe


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parâmetros

*Agreementtype* \[ no\]

Tipo de contrato.

| Valor | Descrição |
|-------|-------------|
| 0 | O pacote de chaves de licença é de um contrato de licença de volume selecionado (para clientes com 250 ou mais computadores). O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado. |
| 1 | O pacote de chaves de licença é de um contrato de licença de volume corporativo para clientes com 250 ou mais computadores. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado. |
| 2 | O pacote de chaves de licença é de um contrato de licença por volume de campus para uma instituição de ensino superior. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado. |
| 3 | O pacote de chaves de licença é de um contrato de licença por volume da escola para instituições primárias e secundárias. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado. |
| 4 | O pacote de chaves de licença é de um contrato de licença de provedor de serviços para provedores de serviços para licenciar softwares da Microsoft mensalmente. O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado. |
| 5 | O pacote de chaves de licença é de outro contrato de licença, como valor aberto, licença aberta de vários anos e licença de assinatura aberta. O parâmetro *sAgreementNumber* é o número do contrato fornecido com as informações do programa. |

*sAgreementNumber* \[ no\]

Número do contrato ou número de registro. O parâmetro *sAgreementNumber* é uma cadeia de caracteres numérica de sete dígitos sem hifens.

*ProductVersion* \[ no\]

Versão do produto.

| Valor | Descrição |
|-------|-------------|
| 0 | Sem suporte |
| 1 | Sem suporte |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ no\]

Tipo de produto.

| Valor | Descrição |
|-------|-------------|
| 0 | O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo. Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença. |
| 1 | O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário. Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença. |
| 2 | Este tipo de produto não é válido. |

*LicenseCount* \[ no\]

Número de licenças a serem instaladas.

*Pacote de chaves* \[ fora\]

Recebe o identificador do pacote de chaves.

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

