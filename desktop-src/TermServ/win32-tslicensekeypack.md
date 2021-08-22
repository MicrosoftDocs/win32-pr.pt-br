---
title: Classe Win32_TSLicenseKeyPack
description: Fornece métodos e propriedades para exibir e instalar Serviços de Área de Trabalho Remota pacotes de chaves de licença.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseKeyPack classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137809"
---
# <a name="win32_tslicensekeypack-class"></a>\_Classe Win32 TSLicenseKeyPack

Fornece métodos e propriedades para exibir e instalar Serviços de Área de Trabalho Remota pacotes de chaves de licença.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSLicenseKeyPack** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSLicenseKeyPack** tem esses métodos.



| Método                                                                                                        | Descrição                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Converte as licenças no pacote de chaves atual.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importações, de outro servidor de licença Área de Trabalho Remota, um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que foi adquirido por meio de uma licença de contrato.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa uma ID de pacote de chaves de licença que foi recebida pela Internet ou pelo telefone.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença aberto.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que foi adquirido por meio de uma loja de varejo.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseKeyPack** tem essas propriedades.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sessão de RD", "sessão de VDI", "Calista", "parceiros de VDI")
</dt> </dl>

Qualificador para direitos de acesso do pacote de chaves de Licenciamento TS

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de licenças disponíveis no pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data de validade do pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de licenças emitidas no pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**Pacote de chaves**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador para o pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**Pacote de chaves**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de pacote de chaves para o servidor de licença Área de Trabalho Remota.

| Valor | Descrição |
|-------|-------------|
| 0 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é desconhecido. |
| 1 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma compra de varejo. |
| 2 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma compra de volume. |
| 3 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma licença simultânea. |
| 4 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é temporário. |
| 5 | O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma licença aberta. |
| 6 | Sem suporte. |

**ProductType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de produto do Serviços de Área de Trabalho Remota pacote de chaves de licença.

| Valor | Descrição |
|-------|-------------|
| 0 | O Serviços de Área de Trabalho Remota tipo de produto do pacote de chaves de licença é por dispositivo. Portanto, cada dispositivo que se conecta ao servidor Host da Sessão RD deve ter uma licença. |
| 1 | O Serviços de Área de Trabalho Remota tipo de produto do pacote de chaves de licença é por usuário. Portanto, cada usuário que se conecta ao servidor Host da Sessão RD deve ter uma licença. |
| 2 | Esse tipo de produto não é válido. |

**Productversion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do produto para o pacote Serviços de Área de Trabalho Remota chave de licença.

| Valor | Descrição |
|-------|-------------|
| "Windows Server 2012" | Somente servidores que executam Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com essa licença. |
| "Windows Server 7" | Somente servidores que executam Windows Server 2008 R2 ou Windows Server 2008 têm suporte com essa licença. |
| "Windows Server 2008" | Somente os servidores que executam Windows Server 2008 têm suporte neste pacote de chaves. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de versão do produto para Serviços de Área de Trabalho Remota pacote de chaves de licença.

| Valor | Descrição |
|-------|-------------|
| 0 | Sem suporte |
| 1 | Sem suporte |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de licenças no pacote Serviços de Área de Trabalho Remota chave de licença.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualificador para o modelo e o tipo de pacote de chaves do Licenciamento do TS. Exemplos: licença de assinatura de VDI por dispositivo, CAL de TS por usuário

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

