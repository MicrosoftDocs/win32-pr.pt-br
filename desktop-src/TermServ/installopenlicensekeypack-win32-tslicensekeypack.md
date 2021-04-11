---
title: Método InstallOpenLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Instala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallOpenLicenseKeyPack
- Método InstallOpenLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454889"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método InstallOpenLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack

Instala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parâmetros

*sLicenseNumber* \[ no\]

Cadeia de caracteres numérica de 8 caracteres fornecida com o pacote de chaves de licença. O parâmetro *sLicenseNumber* não pode conter hifens.

*sAuthorizationNumber* \[ no\]

Cadeia de caracteres alfanumérica de 15 caracteres que é fornecida com a chave de licença. O parâmetro *sAuthorizationNumber* não pode conter hifens.

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
</dt> <dd>

Tipo de produto.

| Valor | Descrição |
|-------|-------------|
| 0 | O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo. Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença. |
| 1 | O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário. Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença. |
| 2 | Este tipo de produto não é válido. |

*LicenseCount* \[ no\]

O número de licenças a serem instaladas.

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

 

